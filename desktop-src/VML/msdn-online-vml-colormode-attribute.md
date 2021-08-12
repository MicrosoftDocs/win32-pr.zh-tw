---
title: VML ColorMode 屬性
description: VML ColorMode 屬性
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81b9b8699ac4806d47581f166dace38f8f724b015b25d18807caa48b44b283e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602139"
---
# <a name="vml-colormode-attribute"></a>VML ColorMode 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定拉伸色彩的模式。 讀取/寫入 **VgTriState**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* colormode = " *expression* " >

**指令碼語法**

 colormode = "*expression*"

*運算式* =** colormode

**備註**

數值包括：



| 值  | 描述                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| 自動   | 指定拉伸的色彩與圖形的填滿色彩相同。 預設值。                |
| 自訂 | 指定拉伸將會是 [color](color-attribute--extrusion--vml.md) 屬性的色彩。 |



 

*Microsoft OfficeExtensions 屬性*

 

 