---
title: Windows 多媒體) 的計時 (
description: 計時
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib，計時
- DrawDibTime 函式
- DrawDib，調試
- 調試 DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688078"
---
# <a name="timing-windows-multimedia"></a>Windows 多媒體) 的計時 (

在偵錯工具中，您可以取得完成重複 DrawDib 作業所需的時間量的相關資訊。 [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime)函數會傳回下列作業的計時資訊：

-   繪製點陣圖
-   解壓縮點陣圖
-   遞色點陣圖
-   延展點陣圖
-   使用 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 函數傳送點陣圖
-   使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 函數傳送點陣圖

在抓取一組值之後， [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) 會重設每項作業的計數和值。

[**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime)函式僅適用于 DrawDib 函數的偵錯工具版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像轉譯](image-rendering.md)
</dt> </dl>

 

 
