---
title: 混音器裝置查詢
description: 混音器裝置查詢
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- 多媒體音訊、混音器裝置查詢
- 音訊、混音器裝置查詢
- 音訊 mixers，裝置查詢
- mixers，裝置查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023415"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="cf264-107">混音器裝置查詢</span><span class="sxs-lookup"><span data-stu-id="cf264-107">Mixer Device Queries</span></span>

<span data-ttu-id="cf264-108">混音器服務提供的函式可判斷系統中的混音器裝置數量，以及裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="cf264-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="cf264-109">您也可以使用混音器服務功能來判斷混音器裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf264-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="cf264-110">您可以使用 [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) 函數來判斷系統中有多少混音器裝置。</span><span class="sxs-lookup"><span data-stu-id="cf264-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="cf264-111">混音器裝置是由裝置識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="cf264-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="cf264-112">裝置識別碼是由指定系統中的裝置數目隱含決定。</span><span class="sxs-lookup"><span data-stu-id="cf264-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="cf264-113">它們的範圍從零到1，小於裝置數目。</span><span class="sxs-lookup"><span data-stu-id="cf264-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="cf264-114">使用混音器裝置之前，您必須先決定其功能。</span><span class="sxs-lookup"><span data-stu-id="cf264-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="cf264-115">音訊功能可能會因一部多媒體電腦而異，因此應用程式需要使用各種不同的音訊硬體。</span><span class="sxs-lookup"><span data-stu-id="cf264-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="cf264-116">您可以使用 [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) 函數來判斷混音器裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="cf264-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="cf264-117">此函式會以指定裝置功能的相關資訊填入 [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) 結構。</span><span class="sxs-lookup"><span data-stu-id="cf264-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="cf264-118">[**MixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)函式會抓取與指定裝置控制碼相關聯的音訊混音器裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf264-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="cf264-119">例如，您可以使用此函式取出音訊混音器的裝置識別碼，然後使用裝置識別碼來調整音量或顯示其他控制項。</span><span class="sxs-lookup"><span data-stu-id="cf264-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 