---
title: 開啟和關閉混音器裝置
description: 開啟和關閉混音器裝置
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- 多媒體音訊，開啟混音器裝置
- 音訊，開啟混音器裝置
- 音訊 mixers，開啟
- mixers，開啟
- 多媒體音訊，關閉混音器裝置
- 音訊，關閉混音器裝置
- 音訊 mixers，關閉
- mixers，關閉
- 開啟混音器裝置
- 關閉混音器裝置
- 裝置識別碼和裝置控制碼
- 音訊 mixers、裝置識別碼和裝置控制碼
- mixers、裝置識別碼和裝置控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023324"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="31c4c-116">開啟和關閉混音器裝置</span><span class="sxs-lookup"><span data-stu-id="31c4c-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="31c4c-117">當您想要使用混音器裝置時，您可以直接使用它，也可以先明確開啟裝置，再使用它。</span><span class="sxs-lookup"><span data-stu-id="31c4c-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="31c4c-118">明確開啟混音器裝置可提供兩個主要優點：</span><span class="sxs-lookup"><span data-stu-id="31c4c-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="31c4c-119">它可保證該混音器裝置持續存在。</span><span class="sxs-lookup"><span data-stu-id="31c4c-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="31c4c-120">它可讓您接收音訊行和控制項變更的通知。</span><span class="sxs-lookup"><span data-stu-id="31c4c-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="31c4c-121">您可以使用 [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) 函式來明確開啟混音器裝置。</span><span class="sxs-lookup"><span data-stu-id="31c4c-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="31c4c-122">此函式會採用裝置識別碼的參數、記憶體位置的指標，以及每種裝置類型獨有的其他值。</span><span class="sxs-lookup"><span data-stu-id="31c4c-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="31c4c-123">記憶體位置會以裝置控制碼填滿。</span><span class="sxs-lookup"><span data-stu-id="31c4c-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="31c4c-124">呼叫其他音訊混音器函式時，請使用此裝置控制碼來識別開啟混音器裝置。</span><span class="sxs-lookup"><span data-stu-id="31c4c-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="31c4c-125">只要混音器裝置的控制碼存在，裝置就會繼續存在於系統中。</span><span class="sxs-lookup"><span data-stu-id="31c4c-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="31c4c-126">如果混音器裝置發生設定變更，但未明確開啟，則您的應用程式可能突然無法存取它。</span><span class="sxs-lookup"><span data-stu-id="31c4c-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="31c4c-127">裝置識別碼和裝置控制碼之間的差異很重要。</span><span class="sxs-lookup"><span data-stu-id="31c4c-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="31c4c-128">當您使用 **mixerOpen** 開啟設備磁碟機時，會傳回裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="31c4c-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="31c4c-129">裝置識別碼是由系統中的裝置數目隱含決定;您可以使用 [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) 函式來取得這個數位。</span><span class="sxs-lookup"><span data-stu-id="31c4c-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="31c4c-130">您可以使用 [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) 函式來關閉混音器裝置。</span><span class="sxs-lookup"><span data-stu-id="31c4c-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="31c4c-131">使用完畢後，您應該關閉裝置。</span><span class="sxs-lookup"><span data-stu-id="31c4c-131">You should close the device after you finish using it.</span></span>

 

 