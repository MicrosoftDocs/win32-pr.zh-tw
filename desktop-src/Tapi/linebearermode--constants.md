---
description: LINEBEARERMODE \_ 位旗標常數描述通話的不同持有人模式。
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: 'LINEBEARERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999515"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="fec2e-103">LINEBEARERMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="fec2e-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="fec2e-104">**LINEBEARERMODE \_** 位旗標常數描述通話的不同持有人模式。</span><span class="sxs-lookup"><span data-stu-id="fec2e-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="fec2e-105">當應用程式進行呼叫時，它可以要求特定的持有人模式。</span><span class="sxs-lookup"><span data-stu-id="fec2e-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="fec2e-106">這些模式可用來針對來自基礎電話網絡的要求連接，選取特定的服務品質。</span><span class="sxs-lookup"><span data-stu-id="fec2e-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="fec2e-107">指定行上可用的持有人模式是線路的裝置功能。</span><span class="sxs-lookup"><span data-stu-id="fec2e-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="fec2e-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**</span><span class="sxs-lookup"><span data-stu-id="fec2e-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-109">相同呼叫 (ISDN) 的其他語音或不受限制資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="fec2e-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="fec2e-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-111">呼叫上不受限制的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="fec2e-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="fec2e-112">資料速率是另外指定的。</span><span class="sxs-lookup"><span data-stu-id="fec2e-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ 多次使用**</span><span class="sxs-lookup"><span data-stu-id="fec2e-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-114">由 ISDN 定義的多次使用模式。</span><span class="sxs-lookup"><span data-stu-id="fec2e-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**</span><span class="sxs-lookup"><span data-stu-id="fec2e-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-116">這會對應至從應用程式到服務提供者或交換器的非通話關聯信號連線， (由 TAPI) 視為媒體串流。</span><span class="sxs-lookup"><span data-stu-id="fec2e-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ 傳遞**</span><span class="sxs-lookup"><span data-stu-id="fec2e-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-118">當呼叫在 LINEBEARERMODE 傳遞中為作用中時 \_ ，服務提供者可讓應用程式直接存取附加的硬體來控制。</span><span class="sxs-lookup"><span data-stu-id="fec2e-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="fec2e-119">這種模式主要是由應用程式 desiring 對非同步數據機的暫時直接控制（透過 [通訊功能](/windows/desktop/DevIO/communications-functions)來存取），以設定或使用服務提供者不支援的特殊功能。</span><span class="sxs-lookup"><span data-stu-id="fec2e-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**</span><span class="sxs-lookup"><span data-stu-id="fec2e-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-121">數位資料的持有人服務，其中每個八位的低序位七位可能包含使用者資料 (例如，用於切換的 56kbit/s 服務) 。</span><span class="sxs-lookup"><span data-stu-id="fec2e-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ 語音**</span><span class="sxs-lookup"><span data-stu-id="fec2e-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-123">這對應于呼叫上的 g. g.711 語音傳輸。</span><span class="sxs-lookup"><span data-stu-id="fec2e-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="fec2e-124">網路可以使用處理技術，例如類比傳輸、回應取消，以及壓縮/解壓縮。</span><span class="sxs-lookup"><span data-stu-id="fec2e-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="fec2e-125">不保證位完整性。</span><span class="sxs-lookup"><span data-stu-id="fec2e-125">Bit integrity is not assured.</span></span> <span data-ttu-id="fec2e-126">語音的目的不是支援傳真和數據機媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fec2e-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec2e-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ 語音**</span><span class="sxs-lookup"><span data-stu-id="fec2e-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fec2e-128">這是標準的 3.1 kHz 類比語音等級持有人服務。</span><span class="sxs-lookup"><span data-stu-id="fec2e-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="fec2e-129">不保證位完整性。</span><span class="sxs-lookup"><span data-stu-id="fec2e-129">Bit integrity is not assured.</span></span> <span data-ttu-id="fec2e-130">語音可以支援傳真和數據機媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fec2e-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fec2e-131">備註</span><span class="sxs-lookup"><span data-stu-id="fec2e-131">Remarks</span></span>

<span data-ttu-id="fec2e-132">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="fec2e-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="fec2e-133">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="fec2e-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="fec2e-134">請注意，持有人模式和媒體類型是不同的概念。</span><span class="sxs-lookup"><span data-stu-id="fec2e-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="fec2e-135">來電的持有人模式是指出網路連線的品質，其主要是由網路所提供。</span><span class="sxs-lookup"><span data-stu-id="fec2e-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="fec2e-136">呼叫的媒體類型表示透過該呼叫交換的資訊資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="fec2e-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="fec2e-137">群組3傳真或資料數據機是使用具有 3.1 kHz 語音持有人模式之呼叫的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="fec2e-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec2e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="fec2e-138">Requirements</span></span>



| <span data-ttu-id="fec2e-139">需求</span><span class="sxs-lookup"><span data-stu-id="fec2e-139">Requirement</span></span> | <span data-ttu-id="fec2e-140">值</span><span class="sxs-lookup"><span data-stu-id="fec2e-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fec2e-141">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fec2e-141">TAPI version</span></span><br/> | <span data-ttu-id="fec2e-142">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fec2e-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fec2e-143">標頭</span><span class="sxs-lookup"><span data-stu-id="fec2e-143">Header</span></span><br/>       | <dl> <span data-ttu-id="fec2e-144"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="fec2e-144"><dt>Tapi.h</dt></span></span> </dl> |



 

