---
title: VML 方向屬性
description: VML 方向屬性
ms.assetid: bf6e0169-f0d4-4dfb-b59e-b5601049fd7a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd7b3f49879f91900682c2e042e500396db7b2d056746037e92f4d590ee1dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124841"
---
# <a name="vml-direction-attribute"></a>VML 方向屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字方塊中文字的方向。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* style = "direction： *expression* " >

**備註**

數值包括：



| 值   | 描述                                                                                |
|---------|--------------------------------------------------------------------------------------------|
| 局部     | 文字會從左至右顯示。 預設值。                                                  |
| Rtl     | 文字由右至左顯示。                                                           |
| 內容 | 指出將以 "coNtext" 值寫出 **MSO 方向的 Alt** 標記。 |



 

*Microsoft OfficeExtensions 屬性*

 

 