---
description: 定義行動寬頻設定檔。
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: 行動寬頻設定檔架構參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82fd085264747807578a260cb7cf0ed254dec7d55a375a77fe022f064e51e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035766"
---
# <a name="mobile-broadband-profile-schema-reference"></a>行動寬頻設定檔架構參考

Mobile 寬頻設定檔架構會定義行動寬頻設定檔。

設定檔儲存行動寬頻連線相關使用者和網路設定參數。 它們也會儲存連接的使用者喜好設定。

行動寬頻設定檔的根項目是 [**MBNProfile**](schema-mbnprofile-element.md) 元素。 每個設定檔都只會有一個根項目。 Windows 7 使用的所有行動寬頻設定檔架構元素都在命名空間中 `https://www.microsoft.com/networking/WWAN/profile/v1` ，而 Windows 8 所使用的元素則位於命名空間中 `https://www.microsoft.com/networking/WWAN/profile/v2` 。

Mobile 寬頻設定檔架構會嚴格地強制執行節點的順序。 設定檔中指定的節點必須遵守行動 **寬頻設定檔架構** ，並且以架構定義中指定的順序顯示。 例如， [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) 必須在 [**AccessString**](schema-accessstring-contexttype-element.md)之後立即指定。

-   [Mobile 寬頻設定檔架構 v1](mobile-broadband-profile-schema.md)
-   [Mobile 寬頻設定檔架構 v2](mobile-broadband-profile-schema-v2.md)
-   [Mobile 寬頻設定檔架構 v3](mobile-broadband-profile-schema-v3.md)
-   [Mobile 寬頻設定檔架構 v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 
