---
description: 裝置管理中會使用下列功能。
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: 裝置管理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936242"
---
# <a name="device-management-functions"></a><span data-ttu-id="59c91-103">裝置管理函式</span><span class="sxs-lookup"><span data-stu-id="59c91-103">Device Management Functions</span></span>

<span data-ttu-id="59c91-104">裝置管理中會使用下列功能。</span><span class="sxs-lookup"><span data-stu-id="59c91-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="59c91-105">函式</span><span class="sxs-lookup"><span data-stu-id="59c91-105">Function</span></span>                                                             | <span data-ttu-id="59c91-106">描述</span><span class="sxs-lookup"><span data-stu-id="59c91-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c91-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="59c91-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="59c91-108">將控制程式代碼直接傳送到指定的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="59c91-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="59c91-109">**InstallNewDevice**</span><span class="sxs-lookup"><span data-stu-id="59c91-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="59c91-110">安裝新的裝置。</span><span class="sxs-lookup"><span data-stu-id="59c91-110">Installs a new device.</span></span> <span data-ttu-id="59c91-111">系統會提示使用者選取裝置。</span><span class="sxs-lookup"><span data-stu-id="59c91-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="59c91-112">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="59c91-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="59c91-113">註冊視窗將接收通知的裝置或裝置類型。</span><span class="sxs-lookup"><span data-stu-id="59c91-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="59c91-114">**UnregisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="59c91-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="59c91-115">關閉指定的裝置通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="59c91-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="59c91-116">下列功能適用于 CD-ROM 和 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="59c91-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="59c91-117">函式</span><span class="sxs-lookup"><span data-stu-id="59c91-117">Function</span></span>                                                               | <span data-ttu-id="59c91-118">描述</span><span class="sxs-lookup"><span data-stu-id="59c91-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c91-119">**CdromDisableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="59c91-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="59c91-120">停用指定 CD-ROM 或 DVD 光碟機的數位播放。</span><span class="sxs-lookup"><span data-stu-id="59c91-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="59c91-121">**CdromEnableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="59c91-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="59c91-122">啟用指定 CD-ROM 或 DVD 光碟機的數位播放。</span><span class="sxs-lookup"><span data-stu-id="59c91-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="59c91-123">**CdromIsDigitalPlaybackEnabled**</span><span class="sxs-lookup"><span data-stu-id="59c91-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="59c91-124">判斷指定的 CD-ROM 或 DVD 光碟機是否已啟用數位播放。</span><span class="sxs-lookup"><span data-stu-id="59c91-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="59c91-125">**CdromKnownGoodDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="59c91-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="59c91-126">判斷指定的 CD-ROM 或 DVD 光碟機是否有已知良好的數位播放。</span><span class="sxs-lookup"><span data-stu-id="59c91-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="59c91-127">**DvdLauncher**</span><span class="sxs-lookup"><span data-stu-id="59c91-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="59c91-128">確認 DVD 光碟機中的媒體區域與 DVD 光碟機區域相符。</span><span class="sxs-lookup"><span data-stu-id="59c91-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
