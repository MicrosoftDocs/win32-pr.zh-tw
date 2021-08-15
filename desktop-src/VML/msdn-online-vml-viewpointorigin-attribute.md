---
title: VML ViewpointOrigin 屬性
description: VML ViewpointOrigin 屬性
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e69357eddfe535b3c6164579454260d8f478430f7a9f1c7bede3262b1b040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007558"
---
# <a name="vml-viewpointorigin-attribute"></a>VML ViewpointOrigin 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

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

*Microsoft OfficeExtensions 屬性*

 

 