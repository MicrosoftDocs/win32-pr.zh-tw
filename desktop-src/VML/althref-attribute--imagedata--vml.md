---
title: 'AltHRef 屬性 (ImageData)  (VML) '
description: 'AltHRef 屬性 (ImageData)  (VML) '
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023662"
---
# <a name="althref-attribute-imagedatavml"></a>AltHRef 屬性 (ImageData)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定影像的替代參考。 讀取/寫入 **字串**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* o:althref = " *expression* " >

**指令碼語法**

 althref = "*expression*"

*運算式* =** althref

**備註**

支援透過 HTML roundtripping 保留 PICT 資料。 在 HTML 寫入時，如果儲存來自 Macintosh) 的檔案，替代表示 (也就是原始的 PICT 資料。 HTML 讀取時， **AltHRef** 優先于 **Src**。

*Microsoft Office Extensions 屬性*

 

 