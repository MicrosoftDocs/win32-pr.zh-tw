---
description: 在特定版本的 Microsoft Windows 上，StretchDIBits 和 SetDIBitsToDevice 函式可讓 JPEG 和 PNG 影像以來源影像的形式傳遞至印表機裝置。
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: 特定點陣圖函式和結構的 JPEG 和 PNG 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625dcde0e673c85dcaef65c2f1aa825121bf871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512876"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>特定點陣圖函式和結構的 JPEG 和 PNG 擴充功能

在特定版本的 Microsoft Windows 上， [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 和 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) 函式可讓 JPEG 和 PNG 影像以來源影像的形式傳遞至印表機裝置。 這個延伸模組並不是用來提供一般 JPEG 和 PNG 解壓縮給應用程式的方法，而是讓應用程式將 JPEG 和 PNG 壓縮影像直接傳送到具有 JPEG 和 PNG 影像硬體支援的印表機。

[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)和 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)結構已擴充，以允許指定表示點陣圖資料為 JPEG 或 PNG 影像的 **biCompression** 值。 只有當 *hdc* 參數指定印表機裝置時，這些壓縮值才會對 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)和 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)有效。 為了支援印表機的中繼檔緩衝，應用程式不應該依賴傳回值來判斷裝置是否支援 JPEG 或 PNG 檔案。 應用程式必須在呼叫 **SetDIBitsToDevice** 和 **StretchDIBits** 之前，使用對應的 escape 來發出 QUERYESCSUPPORT。 如果驗證 escape 失敗，應用程式就必須切換回自己的 JPEG 或 PNG 支援，將影像解壓縮到點陣圖中。

 

 
