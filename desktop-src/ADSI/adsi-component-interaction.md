---
title: ADSI 元件互動
description: Active Directory 路由器元件從用戶端應用程式收到第一個要求時，會從登錄中列出的已安裝 ADSI 提供者填入 ADSI 提供者資料表。
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181104"
---
# <a name="adsi-component-interaction"></a>ADSI 元件互動

Active Directory 路由器元件從用戶端應用程式收到第一個要求時，會從登錄中列出的已安裝 ADSI 提供者填入 ADSI 提供者資料表。 如需登錄的詳細資訊，請參閱 [安裝範例提供者元件](installing-the-example-provider-component.md)。

從目錄對 Active Directory 物件上介面的指標提出要求的作業，是透過函式 (在 C 或 c + +) 的 Visual Basic 或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)中的 **GetObject** ，或 ( [**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)) 的介面方法。 在下圖中，ADSI 用戶端應用程式會將這類 bind 要求傳遞給 ADSI 路由器元件 (1) 。 路由器元件會從 ADsPath 的第一個部分識別提供者的 ProgID，並使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 在登錄 (2) 中尋找相符的 CLSID，並 (3) 載入適當的提供者元件。

![範例提供者中的 adsi 元件互動](images/dscspr.png)

在上圖中，提供者元件會建立代表命名目錄元素的 Active Directory 物件。 ADSI 支援元件會在要求的介面識別碼上進行 **QueryInterface** 。 當該介面的指標被抓取 (4) 時，如同所有的 COM 用戶端/伺服器執行，系統會接著將它傳回給用戶端 (5) ，然後在用戶端應用程式上直接與提供者元件 (6) 一起運作。

 

 