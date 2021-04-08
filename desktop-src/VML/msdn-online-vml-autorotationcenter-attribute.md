---
title: VML AutoRotationCenter 屬性
description: VML AutoRotationCenter 屬性
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682612"
---
# <a name="vml-autorotationcenter-attribute"></a>VML AutoRotationCenter 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定旋轉的中心是否為視角的幾何中心。 讀取/寫入 **VgTriState**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* autorotationcenter = " *expression* " >

**指令碼語法**

 autorotationcenter = "*expression*"

*運算式* =** autorotationcenter

**備註**

拉伸圖形的幾何中心為0、0、0。 如果這個屬性的值為 **False**，則旋轉的中心是由 [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) 屬性所決定。 預設值為 **False**。

*Microsoft Office Extensions 屬性*

 

 