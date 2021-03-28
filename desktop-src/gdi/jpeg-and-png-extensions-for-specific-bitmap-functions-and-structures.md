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
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a><span data-ttu-id="7921a-103">特定點陣圖函式和結構的 JPEG 和 PNG 擴充功能</span><span class="sxs-lookup"><span data-stu-id="7921a-103">JPEG and PNG Extensions for Specific Bitmap Functions and Structures</span></span>

<span data-ttu-id="7921a-104">在特定版本的 Microsoft Windows 上， [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) 和 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) 函式可讓 JPEG 和 PNG 影像以來源影像的形式傳遞至印表機裝置。</span><span class="sxs-lookup"><span data-stu-id="7921a-104">On certain versions of Microsoft Windows, the [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) and [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) functions allow JPEG and PNG images to be passed as the source image to printer devices.</span></span> <span data-ttu-id="7921a-105">這個延伸模組並不是用來提供一般 JPEG 和 PNG 解壓縮給應用程式的方法，而是讓應用程式將 JPEG 和 PNG 壓縮影像直接傳送到具有 JPEG 和 PNG 影像硬體支援的印表機。</span><span class="sxs-lookup"><span data-stu-id="7921a-105">This extension is not intended as a means to supply general JPEG and PNG decompression to applications, but rather to allow applications to send JPEG- and PNG-compressed images directly to printers having hardware support for JPEG and PNG images.</span></span>

<span data-ttu-id="7921a-106">[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)和 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)結構已擴充，以允許指定表示點陣圖資料為 JPEG 或 PNG 影像的 **biCompression** 值。</span><span class="sxs-lookup"><span data-stu-id="7921a-106">The [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) and [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) structures are extended to allow specification of **biCompression** values indicating that the bitmap data is a JPEG or PNG image.</span></span> <span data-ttu-id="7921a-107">只有當 *hdc* 參數指定印表機裝置時，這些壓縮值才會對 [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)和 [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)有效。</span><span class="sxs-lookup"><span data-stu-id="7921a-107">These compression values are only valid for [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) when the *hdc* parameter specifies a printer device.</span></span> <span data-ttu-id="7921a-108">為了支援印表機的中繼檔緩衝，應用程式不應該依賴傳回值來判斷裝置是否支援 JPEG 或 PNG 檔案。</span><span class="sxs-lookup"><span data-stu-id="7921a-108">To support metafile spooling of the printer, the application should not rely on the return value to determine whether the device supports the JPEG or PNG file.</span></span> <span data-ttu-id="7921a-109">應用程式必須在呼叫 **SetDIBitsToDevice** 和 **StretchDIBits** 之前，使用對應的 escape 來發出 QUERYESCSUPPORT。</span><span class="sxs-lookup"><span data-stu-id="7921a-109">The application must issue QUERYESCSUPPORT with the corresponding escape before calling **SetDIBitsToDevice** and **StretchDIBits**.</span></span> <span data-ttu-id="7921a-110">如果驗證 escape 失敗，應用程式就必須切換回自己的 JPEG 或 PNG 支援，將影像解壓縮到點陣圖中。</span><span class="sxs-lookup"><span data-stu-id="7921a-110">If the validation escape fails, the application must then fall back on its own JPEG or PNG support to decompress the image into a bitmap.</span></span>

 

 
