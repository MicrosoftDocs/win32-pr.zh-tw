---
title: 存取控制和讀取作業
description: 安全性是用於搜尋、列舉容器或讀取屬性的隱含篩選。
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- 存取控制和讀取作業 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020751"
---
# <a name="access-control-and-read-operations"></a>存取控制和讀取作業

安全性是用於搜尋、列舉容器或讀取屬性的隱含篩選。 如果您沒有必要的存取權限，則嘗試列出物件或讀取屬性可能會失敗，並出現下列錯誤碼，即使物件或屬性存在也一樣：

-   **E \_ ADS \_ 不正確 \_ 網域 \_ 物件**
-   **\_ \_ \_ 不支援 E ADS \_ 屬性**
-   **\_ \_ \_ \_ 找不到電子 ADS 屬性**

請注意，具有 **\_ \_ ACTRL \_ DS \_ 清單** 存取權之 ADS 的呼叫者可以列舉容器中的子物件。 但是，如果呼叫者沒有 **ADS \_ 右邊 \_ ACTRL \_ DS \_ 清單 \_ 物件** 存取子物件，則嘗試存取子物件仍可能失敗並出現錯誤，例如 **E \_ ADS \_ 未知 \_ 物件**。

安全性對讀取作業的影響不一定會顯示為錯誤。 例如，搜尋作業可能會成功，但是搜尋結果不包含呼叫端沒有存取權的物件或屬性。

 

 




