---
title: 音訊混音器參考
description: 音訊混音器參考
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- 多媒體音訊、音訊 mixers
- 音訊、音訊 mixers
- 多媒體音訊、混音器參考
- 音訊、混音器參考
- 音訊 mixers，參考
- mixers，參考
- 音訊 mixers 的參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185932"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="be6a9-110">音訊混音器參考</span><span class="sxs-lookup"><span data-stu-id="be6a9-110">Audio Mixer Reference</span></span>

<span data-ttu-id="be6a9-111">本節說明與音訊 mixers 相關聯的函式、結構和訊息。</span><span class="sxs-lookup"><span data-stu-id="be6a9-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="be6a9-112">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="be6a9-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="be6a9-113">查詢裝置</span><span class="sxs-lookup"><span data-stu-id="be6a9-113">Querying Devices</span></span>

-   [<span data-ttu-id="be6a9-114">**MIXERCAPS**</span><span class="sxs-lookup"><span data-stu-id="be6a9-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="be6a9-115">**mixerGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="be6a9-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="be6a9-116">**mixerGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="be6a9-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="be6a9-117">開啟和關閉</span><span class="sxs-lookup"><span data-stu-id="be6a9-117">Opening and Closing</span></span>

-   [<span data-ttu-id="be6a9-118">**mixerClose**</span><span class="sxs-lookup"><span data-stu-id="be6a9-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="be6a9-119">**mixerOpen**</span><span class="sxs-lookup"><span data-stu-id="be6a9-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="be6a9-120">正在抓取混音器識別碼</span><span class="sxs-lookup"><span data-stu-id="be6a9-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="be6a9-121">**mixerGetID**</span><span class="sxs-lookup"><span data-stu-id="be6a9-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="be6a9-122">正在抓取線條控制項</span><span class="sxs-lookup"><span data-stu-id="be6a9-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="be6a9-123">**MIXERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="be6a9-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="be6a9-124">**mixerGetLineControls**</span><span class="sxs-lookup"><span data-stu-id="be6a9-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="be6a9-125">**MIXERLINECONTROLS**</span><span class="sxs-lookup"><span data-stu-id="be6a9-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="be6a9-126">變更控制項屬性</span><span class="sxs-lookup"><span data-stu-id="be6a9-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="be6a9-127">**MIXERCONTROLDETAILS**</span><span class="sxs-lookup"><span data-stu-id="be6a9-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="be6a9-128">[**MIXERCONTROLDETAILS \_ 布林值**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be6a9-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="be6a9-129">[**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be6a9-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="be6a9-130">[**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be6a9-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="be6a9-131">[**MIXERCONTROLDETAILS \_ 未簽署**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be6a9-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="be6a9-132">**mixerGetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="be6a9-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="be6a9-133">**mixerSetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="be6a9-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="be6a9-134">正在抓取行資訊</span><span class="sxs-lookup"><span data-stu-id="be6a9-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="be6a9-135">**mixerGetLineInfo**</span><span class="sxs-lookup"><span data-stu-id="be6a9-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="be6a9-136">**MIXERLINE**</span><span class="sxs-lookup"><span data-stu-id="be6a9-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="be6a9-137">**MM \_ MIXM \_ 控制項 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="be6a9-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="be6a9-138">**MM \_ MIXM \_ 行 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="be6a9-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="be6a9-139">傳送 User-Defined 訊息</span><span class="sxs-lookup"><span data-stu-id="be6a9-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="be6a9-140">**mixerMessage**</span><span class="sxs-lookup"><span data-stu-id="be6a9-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="be6a9-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="be6a9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be6a9-142">音訊混音器參考</span><span class="sxs-lookup"><span data-stu-id="be6a9-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 