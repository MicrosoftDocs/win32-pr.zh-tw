---
title: 版本控制和回溯策略
description: 當應用程式使用上述其中一項技術來偵測部分更新，或讀取一組尚未到達其生效日期的物件時，應用程式必須正常地處理這種情況。
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- 版本控制和回溯策略廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55226efcd72cec4f6dbe65447a945733dac88a56b976661bcf24564c9b366ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024409"
---
# <a name="versioning-and-fallback-strategies"></a>版本控制和回溯策略

當應用程式使用上述其中一項技術來偵測部分更新，或讀取一組尚未到達其生效日期的物件時，應用程式必須正常地處理這種情況。 對於某些應用程式而言，適當的回應是「切換回」先前的物件版本。 Active Directory Domain Services 不提供版本控制功能，則需要這項功能的應用程式必須自行提供。 版本控制的方法包括將「最後已知的良好」值保留在本機快取，並在目錄中儲存多組物件，例如在「舊」、「目前」和「新」容器中。 可能有許多其他架構。

執行必須小心避免非預期的結果。 只有在偵測到部分更新或新物件尚未「生效」時，才應該使用舊版的物件。 由於應用程式「無法運作」中的某些內容，可能會規避系統管理員的意圖。 例如，兩部先前可以通訊的電腦可能會因為網際網路通訊協定安全性 (IPsec) 原則的變更，而發現自己無法這麼做。 如果這是系統管理員的一部分，受影響的系統不應該回復至允許它們進行通訊的原則，因為這會造成安全性缺口。

 

 




