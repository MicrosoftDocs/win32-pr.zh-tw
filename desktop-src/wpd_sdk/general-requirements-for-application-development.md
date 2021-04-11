---
description: 應用程式開發的一般需求
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: 應用程式開發 (WPD API) 的一般需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193548"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="f50f2-103">應用程式開發 (WPD API) 的一般需求</span><span class="sxs-lookup"><span data-stu-id="f50f2-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="f50f2-104">若要建立 Windows 可攜式裝置應用程式，您必須在電腦上安裝 [Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads) 。</span><span class="sxs-lookup"><span data-stu-id="f50f2-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="f50f2-105">必要的標頭和程式庫會出現在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="f50f2-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="f50f2-106">PortableDeviceGuids .lib</span><span class="sxs-lookup"><span data-stu-id="f50f2-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="f50f2-107">PortableDevice。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-107">PortableDevice.h</span></span>
-   <span data-ttu-id="f50f2-108">PortableDeviceTypes。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="f50f2-109">PortableDeviceApi。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="f50f2-110">應用程式所需的任何其他必要程式庫和標頭，以取用或轉譯媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="f50f2-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="f50f2-111">如果您的應用程式支援新的裝置服務介面，它也會包含下列一或多個標頭檔。</span><span class="sxs-lookup"><span data-stu-id="f50f2-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="f50f2-112">AnchorSyncDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-113">BridgeDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-114">CalendarDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-115">ContactDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-116">DeviceServices。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-116">DeviceServices.h</span></span>
-   <span data-ttu-id="f50f2-117">FullEnumSyncDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-118">HintsDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-119">MessageDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-120">MetadataDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-121">NotesDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-122">RingtoneDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-123">StatusDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-124">SyncDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="f50f2-125">TaskDeviceService。h</span><span class="sxs-lookup"><span data-stu-id="f50f2-125">TaskDeviceService.h</span></span>

<span data-ttu-id="f50f2-126">在上述清單中，幾乎所有支援裝置服務的應用程式都需要 BridgeDeviceService .h 和 DeviceService。其他檔案會定義不同類型的裝置服務，並且會適當地納入。</span><span class="sxs-lookup"><span data-stu-id="f50f2-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f50f2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f50f2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50f2-128">**Windows 可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="f50f2-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
