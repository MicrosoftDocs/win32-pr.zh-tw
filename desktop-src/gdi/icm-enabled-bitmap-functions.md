---
description: Microsoft 影像色彩管理 (ICM) 可確保色彩影像、繪圖物件或文字物件在任何裝置上都能盡可能地轉譯成其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled 點陣圖函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848551"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="3e052-103">ICM-Enabled 點陣圖函數</span><span class="sxs-lookup"><span data-stu-id="3e052-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="3e052-104">Microsoft 影像色彩管理 (ICM) 可確保色彩影像、繪圖物件或文字物件在任何裝置上都能盡可能地轉譯成其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。</span><span class="sxs-lookup"><span data-stu-id="3e052-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="3e052-105">無論您是要掃描彩色掃描器上的影像或其他圖形、在螢幕上進行觀看或編輯，或是列印在紙張、電影或其他媒體上，ICM 2.0 都能協助您保持一致且精確的色彩。</span><span class="sxs-lookup"><span data-stu-id="3e052-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="3e052-106">如需 ICM 的詳細資訊，請參閱 [Windows 色彩系統](/previous-versions//dd372446(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3e052-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="3e052-107">圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。</span><span class="sxs-lookup"><span data-stu-id="3e052-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="3e052-108">下列點陣圖函數可用於 ICM：</span><span class="sxs-lookup"><span data-stu-id="3e052-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="3e052-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="3e052-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="3e052-110">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="3e052-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="3e052-111">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="3e052-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="3e052-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="3e052-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="3e052-113">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="3e052-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="3e052-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="3e052-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="3e052-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="3e052-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="3e052-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="3e052-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="3e052-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="3e052-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
