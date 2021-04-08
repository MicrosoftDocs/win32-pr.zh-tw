---
title: VML Specularity 屬性
description: VML Specularity 屬性
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b4e8814a9bd0cd897ae018cf8b37aa67d732aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842463"
---
# <a name="vml-specularity-attribute"></a>VML Specularity 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義拉伸圖形的 specularity。 讀取/寫入 **VgNumber**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* specularity = " *expression* " >

**指令碼語法**

 specularity = "*expression*"

*運算式* =** specularity

**備註**

此值會定義事件光線對反射反映光線的比率。 標準值的範圍是從0到1。 預設值為 0。

如果指定大於1的值，則可能會產生不尋常的效果。

Microsoft Office Extensions 屬性

 

 