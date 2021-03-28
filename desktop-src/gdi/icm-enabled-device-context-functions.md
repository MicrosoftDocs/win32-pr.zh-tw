---
description: Microsoft 影像色彩管理 (ICM) 可確保色彩影像、圖形或文字物件在任何裝置上都能盡可能地轉譯為其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled 裝置內容函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972664"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="fdd32-103">ICM-Enabled 裝置內容函式</span><span class="sxs-lookup"><span data-stu-id="fdd32-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="fdd32-104">Microsoft 影像色彩管理 (ICM) 可確保色彩影像、圖形或文字物件在任何裝置上都能盡可能地轉譯為其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。</span><span class="sxs-lookup"><span data-stu-id="fdd32-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="fdd32-105"> (需詳細資訊，請參閱 [Windows Color System](/previous-versions//dd372446(v=vs.85)). ) </span><span class="sxs-lookup"><span data-stu-id="fdd32-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="fdd32-106">圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。</span><span class="sxs-lookup"><span data-stu-id="fdd32-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="fdd32-107">下列裝置內容函式已啟用以搭配 ICM 使用：</span><span class="sxs-lookup"><span data-stu-id="fdd32-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="fdd32-108">**CreateCompatibleDC**</span><span class="sxs-lookup"><span data-stu-id="fdd32-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="fdd32-109">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="fdd32-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="fdd32-110">**GetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="fdd32-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="fdd32-111">**GetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="fdd32-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="fdd32-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="fdd32-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="fdd32-113">**SelectObject**</span><span class="sxs-lookup"><span data-stu-id="fdd32-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="fdd32-114">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="fdd32-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="fdd32-115">**SetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="fdd32-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
