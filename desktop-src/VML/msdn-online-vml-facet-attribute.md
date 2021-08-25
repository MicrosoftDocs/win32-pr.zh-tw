---
title: VML Facet 屬性
description: VML Facet 屬性
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681008"
---
# <a name="vml-facet-attribute"></a>VML Facet 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義用來描述拉伸曲線表面的 facet 數目。 讀取/寫入 **VgNumber**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* facet = " *expression* " >

**指令碼語法**

*元素* 。 facet = "*expression*"

*運算式* =*元素*。 facet

**備註**

定義轉譯引擎將接近延伸的方式。 較低的數位會表示轉譯引擎的轉譯容錯較低，而且會產生更多 facet。 較高的數位會讓您的延伸顯示更多面向。 預設值為30000。

*Microsoft OfficeExtensions 屬性*

 

 