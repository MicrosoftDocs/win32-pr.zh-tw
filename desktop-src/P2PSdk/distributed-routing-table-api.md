---
description: 分散式路由表 (的 DRT) API 可讓應用程式在對等網路中發佈及解析數位金鑰。
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: 分散式路由資料表 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026757"
---
# <a name="distributed-routing-table-api"></a>分散式路由資料表 API

分散式路由表 (的 DRT) API 可讓應用程式在對等網路中發佈及解析數位金鑰。

利用 DRT 的應用程式可以完成下列工作：

-   建立應用程式特定的分散式路由表。
-   註冊金鑰，並將這些金鑰與 IP 位址和應用程式資料產生關聯。
-   搜尋金鑰，並取得與它們相關聯的 IP 位址和應用程式資料。 這項功能可以用來建立分散式雜湊表 (DHTs) 、無伺服器名稱解析系統，以及許多拓撲的重迭網格網路。

> [!Note]  
> 系統管理員和已啟用 DRT 的應用程式使用者應該讓其應用程式的使用者知道所發佈的資訊。 本技術未採用 microsoft 伺服器，而且資訊不會傳送給 Microsoft。

 

為此 API 提供的檔分為三個部分。



| 區段                                                                                | 描述                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [關於分散式路由表](about-distributed-routing-tables.md)               | 詳述 DRT API 生命週期和狀態變更的資訊。<br/>                                    |
| [使用分散式路由資料表 API](using-the-distributed-routing-table-api.md) | 詳細說明的是如何使用的「DRT API」。<br/>                                                   |
| [分散式路由資料表 API 參考](distributed-routing-table-api-reference.md) | 詳細說明組成 DRT API 的函式、資料結構和列舉常數的資訊。<br/> |



 

 

 




