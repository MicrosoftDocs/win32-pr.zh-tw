---
title: VML Diffusity 屬性
description: VML Diffusity 屬性
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a8e51750bcd71421609221812eb38bbf709657
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001081"
---
# <a name="vml-diffusity-attribute"></a>VML Diffusity 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義來自拉伸形狀的已反射光源的擴散量。 讀取/寫入 **VgNumber**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* diffusity = " *expression* " >

**指令碼語法**

 diffusity = "*expression*"

*運算式* =** diffusity

**備註**

此值會定義事件光線與漫射反映燈光之間的比率。 標準值的範圍是從0到1。 預設值為 0。

如果指定大於1的值，則可能會產生不尋常的效果。

*Microsoft Office Extensions 屬性*

 

 