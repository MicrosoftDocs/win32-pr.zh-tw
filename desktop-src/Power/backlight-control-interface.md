---
description: 背光控制項介面是標準化的 IOCTL 介面，用來控制 LCD 背光的亮度。
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: 背光控制項介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977910"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="df8a0-103">背光控制項介面</span><span class="sxs-lookup"><span data-stu-id="df8a0-103">Backlight Control Interface</span></span>

<span data-ttu-id="df8a0-104">背光控制項介面是標準化的 IOCTL 介面，用來控制 LCD 背光的亮度。</span><span class="sxs-lookup"><span data-stu-id="df8a0-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="df8a0-105">需要以程式設計方式控制背光亮度或為使用者提供控制項的應用程式，應該使用此介面，而不是使用專屬的介面;否則，系統無法查詢目前的硬體亮度，而且可能會變成未同步處理。</span><span class="sxs-lookup"><span data-stu-id="df8a0-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="df8a0-106">第一個步驟是使用 [**IOCTL \_ VIDEO \_ 查詢 \_ 支援的 \_ 亮度**](ioctl-video-query-supported-brightness.md) 控制程式代碼，查詢裝置以取得支援的亮度。</span><span class="sxs-lookup"><span data-stu-id="df8a0-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="df8a0-107">此作業會傳回指定可用亮度層級的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="df8a0-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="df8a0-108">接下來，您可以使用 [**IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度**](ioctl-video-query-display-brightness.md) 控制項程式碼，查詢裝置以取得目前的顯示器亮度。</span><span class="sxs-lookup"><span data-stu-id="df8a0-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="df8a0-109">此作業會傳回目前的設定，以替代目前的 (AC) 亮度、直接目前 (DC) 亮度和電源狀態。</span><span class="sxs-lookup"><span data-stu-id="df8a0-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="df8a0-110">若要變更顯示器亮度，請使用 [**IOCTL \_ VIDEO \_ SET \_ 顯示器 \_ 亮度**](ioctl-video-set-display-brightness.md) 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="df8a0-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="df8a0-111">您可以設定 AC 亮度、DC 亮度或兩者。</span><span class="sxs-lookup"><span data-stu-id="df8a0-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df8a0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="df8a0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df8a0-113">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="df8a0-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



