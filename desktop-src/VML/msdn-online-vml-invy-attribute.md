---
title: VML InvY 屬性
description: VML InvY 屬性
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315535"
---
# <a name="vml-invy-attribute"></a>VML InvY 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷控制碼的 y 位置是否反轉。 讀取/寫入 **VgTriState**。

**適用於**

[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) 

**標記語法**

<v： *element* invy = " *expression* " >

**備註**

若 **為 True**，則會將控制碼的 y 位置從 **CoordOrigin** 的 y 值減去 **CoordSize** 的 y 值，以反轉方向。 預設值為 **[False]** 。

這個屬性等同于


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*VML 標準屬性*

 

 