---
title: 使用 ASP.NET Core 和 Azure 的 DevOps |接下來的步驟
author: CamSoper
description: 本指南為如何為 Azure 上裝載的 ASP.NET Core 應用程式，建置 DevOps 管線的完整指導。
ms.author: casoper
ms.date: 08/07/2018
uid: azure/devops/next-steps
ms.openlocfilehash: 7a0f1b1b56a33b1870e0657d8ba465adb84f5a02
ms.sourcegitcommit: d53e0cc71542b92de867bcce51575b054886f529
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/16/2018
ms.locfileid: "42909638"
---
# <a name="next-steps"></a>後續步驟

在本指南中，您可以建立 ASP.NET Core 範例應用程式的 DevOps 管線。 恭喜您！ 我們希望您滿意學習服務來發佈至 Azure App Service 的 ASP.NET Core web 應用程式，並自動執行變更的持續整合。

除了 web 裝載及 DevOps，Azure 會有各式各樣的平台為-即服務 (PaaS) 服務的 ASP.NET Core 開發人員很有用。 本節提供的一些最常使用的服務的簡短概觀。

## <a name="storage-and-databases"></a>儲存體和資料庫

[Redis 快取](https://docs.microsoft.com/azure/redis-cache/)是高輸送量、 低延遲的資料快取 以服務形式提供。 它可以用於快取頁面輸出，而降低資料庫的要求，並且提供多個執行個體的應用程式的 ASP.NET Core 工作階段狀態。

[Azure 儲存體](https://docs.microsoft.com/azure/storage/)是 Azure 的可大幅調整的雲端儲存體。 開發人員可以利用[佇列儲存體](https://docs.microsoft.com/azure/storage/queues/storage-queues-introduction)可靠的訊息佇列，並[表格儲存體](https://docs.microsoft.com/azure/storage/tables/table-storage-overview)是專為使用大量半結構化資料集的快速開發所設計的 NoSQL 索引鍵-值存放區。

[Azure SQL Database](https://docs.microsoft.com/azure/sql-database/)提供熟悉的關聯式資料庫即服務，使用 Microsoft SQL Server 引擎的功能。

[Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/)全域散發的多模型 NoSQL 資料庫服務。 多個 Api 已推出，包括 SQL API （先前稱為 DocumentDB）、 Cassandra 和 MongoDB。

## <a name="identity"></a>身分識別

[Azure Active Directory](https://docs.microsoft.com/azure/active-directory/)並[Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/)是這兩個身分識別服務。 Azure Active Directory 專為企業案例，和預期的商務-客戶案例，包括社交網路登入 Azure Active Directory B2C 時，可讓 Azure AD B2B （企業對企業） 共同作業。

## <a name="mobile"></a>行動訊息

[通知中樞](https://docs.microsoft.com/azure/notification-hubs/)是多平台、 可調整的推播通知引擎，快速地將數百萬則訊息傳送至各種類型的裝置上執行的應用程式。

## <a name="web-infrastructure"></a>Web 基礎結構

[Azure Container Service](https://docs.microsoft.com/azure/aks/)管理裝載的 Kubernetes 的環境，讓您快速而且容易部署及管理容器化應用程式，而不需要容器協調流程專業知識。

[Azure 搜尋服務](https://docs.microsoft.com/azure/search/)用來建立私人和異質性內容上的企業搜尋解決方案。

[Service Fabric](https://docs.microsoft.com/azure/service-fabric/)是分散式的系統平台，可讓您輕鬆封裝、 部署及管理可調整且可靠的微服務以及容器。
