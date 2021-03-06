---
uid: mvc/overview/getting-started/database-first-development/changing-the-database
title: EF Database First 與 ASP.NET MVC： 變更資料庫 |Microsoft Docs
author: tfitzmac
description: 您可以使用 MVC、 Entity Framework 和 ASP.NET Scaffolding，來建立 web 應用程式，提供介面給現有的資料庫。 本教學課程的里...
ms.author: riande
ms.date: 10/01/2014
ms.assetid: cfd5c083-a319-482e-8f25-5b38caa93954
msc.legacyurl: /mvc/overview/getting-started/database-first-development/changing-the-database
msc.type: authoredcontent
ms.openlocfilehash: 4ee73dc066a56944dd2e5600460628656ae87e37
ms.sourcegitcommit: 45ac74e400f9f2b7dbded66297730f6f14a4eb25
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/16/2018
ms.locfileid: "41831172"
---
<a name="ef-database-first-with-aspnet-mvc-changing-the-database"></a>EF Database First 與 ASP.NET MVC： 變更資料庫
====================
藉由[Tom FitzMacken](https://github.com/tfitzmac)

> 您可以使用 MVC、 Entity Framework 和 ASP.NET Scaffolding，來建立 web 應用程式，提供介面給現有的資料庫。 本系列教學課程會示範如何自動產生程式碼，可讓使用者顯示、 編輯、 建立及刪除位於資料庫資料表中的資料。 產生的程式碼會對應至資料庫資料表中的資料行。
> 
> 系列的這個部分會著重於對資料庫結構的更新和傳播該項變更整個 web 應用程式。


## <a name="add-a-column"></a>加入資料行

如果您在資料庫中更新資料表的結構，您需要確保您的變更會傳播到資料模型、 檢視和控制器。

本教學課程中，要將新的資料行加入記錄中間名學生的 Student 資料表中。 若要新增此資料行，請開啟資料庫專案，並開啟 Student.sql 檔案。 透過設計工具或 T-SQL 程式碼中，新增名為的資料行**MiddleName** NVARCHAR(50) 且允許 NULL 值。

![新增中間名](changing-the-database/_static/image1.png)

啟動您的資料庫專案 （或 F5），這項變更部署到您的本機資料庫。 新的欄位加入至資料表。 如果您看不到 SQL Server 物件總管 中，按一下窗格中的 重新整理 按鈕。

![顯示新的資料行](changing-the-database/_static/image2.png)

新的資料行存在於資料庫資料表中，但它目前不存在的資料模型類別中。 您必須更新模型，以包含新的資料行。 在 **模型**資料夾中，開啟**ContosoModel.edmx**檔案來顯示模型圖表。 請注意，Student 模型不包含 [MiddleName] 屬性。 以滑鼠右鍵按一下設計介面上的任何位置，然後選取**從資料庫更新模型**。

![更新模型](changing-the-database/_static/image3.png)

在 [更新精靈] 中，選取**重新整理**索引標籤和**學生**資料表。

![更新精靈](changing-the-database/_static/image4.png)

按一下 [ **完成**]。

在更新程序完成之後，資料庫圖表包含新**MiddleName**屬性。 儲存**ContosoModel.edmx**檔案。 您必須儲存此檔案才能傳播至新的屬性**Student.cs**類別。 您現在已更新的資料庫和模型。

建置方案。

不幸的是，在檢視仍然不包含新的屬性。 若要更新的檢視有兩個選項-您可以重新產生檢視藉由再次新增 scaffold Student 類別，或您可以手動將新屬性新增至您現有的檢視。 在本教學課程中，您會新增 scaffolding 再次因為您無法對任何自訂的變更自動產生的檢視。 您可以考慮以手動方式加入的屬性，當您檢視已變更，並不想要捨棄這些變更。

若要確保檢視時都會重新建立**學生**下方的資料夾**檢視**，並刪除**StudentsController**。 然後，以滑鼠右鍵按一下**控制器**資料夾，並新增樣板**學生**模型。 同樣地，將控制器命名**StudentsController**。 選取 [確定]。

檢視現在會包含 [MiddleName] 屬性。

![顯示中間名](changing-the-database/_static/image5.png)

在下一步 區段中，您將加入程式碼來自訂顯示學生記錄的詳細檢視。

> [!div class="step-by-step"]
> [上一頁](generating-views.md)
> [下一頁](customizing-a-view.md)
