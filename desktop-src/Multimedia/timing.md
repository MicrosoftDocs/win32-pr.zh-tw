---
title: Windows 多媒體)  (時間
description: 計時
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib，計時
- DrawDibTime 函式
- DrawDib，調試
- 調試 DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464072"
---
# <a name="timing-windows-multimedia"></a>Windows 多媒體)  (時間

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

 

 
