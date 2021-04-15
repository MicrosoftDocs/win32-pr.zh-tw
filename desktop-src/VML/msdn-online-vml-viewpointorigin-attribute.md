---
title: VML ViewpointOrigin 屬性
description: VML ViewpointOrigin 屬性
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463280"
---
# <a name="vml-viewpointorigin-attribute"></a>VML ViewpointOrigin 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形周框方塊內的觀點原點。 讀取/寫入 **VgVector2D**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* viewpointorigin = " *expression* " >

**指令碼語法**

 viewpointorigin = "*expression*"

*運算式* =** viewpointorigin

**備註**

根據原始圖形的 x 和 y 值來定義觀點。 X 和 y 值的範圍是從0.5 到-0.5 (50% 到圖形座標原點) 的50%。 預設值為0，0。

*Microsoft Office Extensions 屬性*

 

 