---
description: 視窗裝置內容可讓應用程式在視窗中的任何位置繪製，包括非工作區。
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: 視窗顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75abed6177771d9beff56ad5e7dec1f8e0a704c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973056"
---
# <a name="window-display-device-contexts"></a>視窗顯示裝置內容

*視窗裝置內容* 可讓應用程式在視窗中的任何位置繪製，包括非工作區。 使用自訂非工作區的應用程式，通常會使用視窗裝置內容來處理適用于 windows 的 [**wm \_ NCPAINT**](wm-ncpaint.md) 和 [**WM \_ NCACTI加值稅E**](../winmsg/wm-ncactivate.md) 訊息。 不建議針對任何其他用途使用視窗裝置內容。

應用程式可以使用 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函數，並指定 DCX 視窗選項，以抓取視窗裝置內容 \_ 。 此函式會從顯示裝置內容快取抓取視窗裝置內容。 使用視窗裝置內容的視窗，必須儘快使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放它。 視窗裝置內容一律來自快取;CS \_ OWNDC 和 cs \_ CLASSDC 類別的樣式不會影響裝置內容。

當應用程式抓取視窗裝置內容時，系統會將裝置原點設定為視窗的左上角，而不是工作區的左上角。 它也會設定裁剪區域以包含整個視窗，而不只是工作區。 系統會將視窗裝置內容的目前屬性值設定為與一般裝置內容相同的預設值。 應用程式可以變更屬性值，但在釋放裝置內容時，系統不會保留任何變更。

 

 
