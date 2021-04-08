---
title: 一致性 Guid
description: 一致性 Guid 是一種偵測策略，可讓應用程式偵測部分更新。
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020742"
---
# <a name="consistency-guids"></a>一致性 Guid

一致性 Guid 是一種偵測策略，可讓應用程式偵測部分更新。 一致性 GUID (全域唯一識別碼) 會套用至相關集合中的每個物件。 在執行時，來源應用程式會產生新的 GUID，並將其套用至它在相關物件集中更新的每一個物件。 然後，它會將新的 GUID 套用至集合中其餘的物件，並將新的 GUID 套用至 "master" 物件來完成。 一般而言，「主要」物件會是容器，也就是集合中其他物件的父系。

一些重要考量︰

-   與物件計數或總和檢查碼結合的一致性 Guid 比一致性 Guid 更有效率，因為讀取物件的應用程式可能不知道有多少物件有 GUID 存在。
-   應用程式必須產生自己的 Guid (Microsoft WIN32 API （UuidCreate）提供此函式) ，而不使用在物件的 **objectGUID** 屬性中找到的系統產生的 guid。 這是因為每次更新物件集時，一致性 GUID 都需要變更。 在 **objectGUID** 中找到的物件識別 guid 永遠不會在建立物件之後變更。
-   一致性 Guid 假設不會在集合之間共用任何物件，因此每個集合都可以有唯一的一致性 GUID。

 

 




