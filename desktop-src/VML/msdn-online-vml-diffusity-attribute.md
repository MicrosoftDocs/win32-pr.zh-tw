---
title: VML Diffusity 屬性
description: VML Diffusity 屬性
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b311c70e1cf49ece7f0072d70b07e886d11f0fe9122fc5d248a32f4321ba19b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754732"
---
# <a name="vml-diffusity-attribute"></a>VML Diffusity 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

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

*Microsoft OfficeExtensions 屬性*

 

 