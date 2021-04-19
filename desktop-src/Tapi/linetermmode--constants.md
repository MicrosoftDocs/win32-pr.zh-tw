---
description: LINETERMMODE \_ 位旗標常數描述可路由傳送至終端機裝置的電話線路上不同類型的事件。
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: 'LINETERMMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998770"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="8440f-103">LINETERMMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="8440f-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="8440f-104">**LINETERMMODE \_** 位旗標常數描述可路由傳送至終端機裝置的電話線路上不同類型的事件。</span><span class="sxs-lookup"><span data-stu-id="8440f-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="8440f-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE \_ 按鈕**</span><span class="sxs-lookup"><span data-stu-id="8440f-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-106">這些是從終端機傳送至該行的按鍵事件。</span><span class="sxs-lookup"><span data-stu-id="8440f-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="8440f-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-108">這會顯示從該行傳送到終端機的資訊。</span><span class="sxs-lookup"><span data-stu-id="8440f-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="8440f-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-110">這些是從終端機傳送至該行的 hookswitch 事件。</span><span class="sxs-lookup"><span data-stu-id="8440f-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE \_ 燈**</span><span class="sxs-lookup"><span data-stu-id="8440f-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-112">這些是從該行傳送到終端機的燈光事件。</span><span class="sxs-lookup"><span data-stu-id="8440f-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="8440f-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-114">這是與線條和終端機上的呼叫相關聯的雙向媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="8440f-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="8440f-115">當呼叫之媒體資料流程的單向通道的路由無法獨立控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="8440f-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**</span><span class="sxs-lookup"><span data-stu-id="8440f-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-117">這是從線條到與線路上的呼叫相關聯的終端機的單向媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="8440f-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="8440f-118">當呼叫之媒體資料流程的單向通道的路由可以獨立控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="8440f-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**</span><span class="sxs-lookup"><span data-stu-id="8440f-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-120">這是從終端機到與該行通話相關聯之線條的單向媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="8440f-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="8440f-121">當呼叫之媒體資料流程的單向通道的路由可以獨立控制時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="8440f-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8440f-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ 響鈴**</span><span class="sxs-lookup"><span data-stu-id="8440f-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8440f-123">這是從交換器傳送到終端機的響鈴控制資訊。</span><span class="sxs-lookup"><span data-stu-id="8440f-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8440f-124">備註</span><span class="sxs-lookup"><span data-stu-id="8440f-124">Remarks</span></span>

<span data-ttu-id="8440f-125">無延伸。</span><span class="sxs-lookup"><span data-stu-id="8440f-125">No extensibility.</span></span> <span data-ttu-id="8440f-126">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="8440f-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="8440f-127">這些常數描述可直接線上路裝置與終端機裝置 (（例如電話組) ）之間路由的控制項和資訊資料流程的類別。</span><span class="sxs-lookup"><span data-stu-id="8440f-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="8440f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8440f-128">Requirements</span></span>



| <span data-ttu-id="8440f-129">需求</span><span class="sxs-lookup"><span data-stu-id="8440f-129">Requirement</span></span> | <span data-ttu-id="8440f-130">值</span><span class="sxs-lookup"><span data-stu-id="8440f-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8440f-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8440f-131">TAPI version</span></span><br/> | <span data-ttu-id="8440f-132">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8440f-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8440f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8440f-133">Header</span></span><br/>       | <dl> <span data-ttu-id="8440f-134"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="8440f-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 




