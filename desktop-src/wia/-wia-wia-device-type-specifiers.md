---
description: Windows 映像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: WIA 裝置類型規範
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997492"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="72bc1-103">WIA 裝置類型規範</span><span class="sxs-lookup"><span data-stu-id="72bc1-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="72bc1-104">Windows 映像取得 (WIA) 裝置類型規範是指出附加至使用者電腦之裝置類型的常數。</span><span class="sxs-lookup"><span data-stu-id="72bc1-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="72bc1-105">使用 GET \_ STIDEVICE \_ TYPE 宏從 WIA 裝置類型屬性取得這些值。</span><span class="sxs-lookup"><span data-stu-id="72bc1-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="72bc1-106">以下是有效的 WIA 裝置類型規範：</span><span class="sxs-lookup"><span data-stu-id="72bc1-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="72bc1-107">裝置類型</span><span class="sxs-lookup"><span data-stu-id="72bc1-107">Device Type</span></span>                 | <span data-ttu-id="72bc1-108">意義</span><span class="sxs-lookup"><span data-stu-id="72bc1-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bc1-109">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="72bc1-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="72bc1-110">一般 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="72bc1-110">Generic WIA device.</span></span> <span data-ttu-id="72bc1-111">在裝置列舉期間，會使用這個常數來列舉所有的 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="72bc1-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="72bc1-112">StiDeviceTypeDigitalCamera</span><span class="sxs-lookup"><span data-stu-id="72bc1-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="72bc1-113">裝置是相機。</span><span class="sxs-lookup"><span data-stu-id="72bc1-113">The device is a camera.</span></span> <span data-ttu-id="72bc1-114">*不支援這個規範* Windows Vista （含） *以後版本。*</span><span class="sxs-lookup"><span data-stu-id="72bc1-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="72bc1-115">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="72bc1-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="72bc1-116">裝置是掃描器。</span><span class="sxs-lookup"><span data-stu-id="72bc1-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="72bc1-117">StiDeviceTypeStreamingVideo</span><span class="sxs-lookup"><span data-stu-id="72bc1-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="72bc1-118">裝置包含串流影片。</span><span class="sxs-lookup"><span data-stu-id="72bc1-118">The device contains streaming video.</span></span> <span data-ttu-id="72bc1-119">*不支援這個規範* Windows Server 2003 *、* windows Vista *或更新版本。*</span><span class="sxs-lookup"><span data-stu-id="72bc1-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



