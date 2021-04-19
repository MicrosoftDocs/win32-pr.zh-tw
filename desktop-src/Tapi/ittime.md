---
description: ITTime 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: 'ITTime 介面 (Sdpblb .h) '
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995258"
---
# <a name="ittime-interface"></a><span data-ttu-id="f6c03-103">ITTime 介面</span><span class="sxs-lookup"><span data-stu-id="f6c03-103">ITTime interface</span></span>

<span data-ttu-id="f6c03-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="f6c03-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6c03-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f6c03-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6c03-106">**ITTime** 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。</span><span class="sxs-lookup"><span data-stu-id="f6c03-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="f6c03-107">它可讓您存取會話的一組啟用時間。</span><span class="sxs-lookup"><span data-stu-id="f6c03-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="f6c03-108">[**IEnumTime：： Next**](ienumtime-next.md)和 [**ITTimeCollection：： create**](ittimecollection-create.md)方法會建立 **ITTime** 介面。</span><span class="sxs-lookup"><span data-stu-id="f6c03-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="f6c03-109">成員</span><span class="sxs-lookup"><span data-stu-id="f6c03-109">Members</span></span>

<span data-ttu-id="f6c03-110">**ITTime** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="f6c03-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f6c03-111">**ITTime** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6c03-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="f6c03-112">方法</span><span class="sxs-lookup"><span data-stu-id="f6c03-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f6c03-113">方法</span><span class="sxs-lookup"><span data-stu-id="f6c03-113">Methods</span></span>

<span data-ttu-id="f6c03-114">**ITTime** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f6c03-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="f6c03-115">方法</span><span class="sxs-lookup"><span data-stu-id="f6c03-115">Method</span></span>                                         | <span data-ttu-id="f6c03-116">描述</span><span class="sxs-lookup"><span data-stu-id="f6c03-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="f6c03-117">**取得 \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="f6c03-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="f6c03-118">取得32位 NTP (網路時間通訊協定) 開始時間值。</span><span class="sxs-lookup"><span data-stu-id="f6c03-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="f6c03-119">**取得 \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="f6c03-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="f6c03-120">取得 NTP 結束時間值。</span><span class="sxs-lookup"><span data-stu-id="f6c03-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="f6c03-121">**put \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="f6c03-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="f6c03-122">設定32位 NTP 開始時間值。</span><span class="sxs-lookup"><span data-stu-id="f6c03-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="f6c03-123">**put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="f6c03-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="f6c03-124">設定 NTP 結束時間值。</span><span class="sxs-lookup"><span data-stu-id="f6c03-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="f6c03-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6c03-125">Requirements</span></span>



| <span data-ttu-id="f6c03-126">需求</span><span class="sxs-lookup"><span data-stu-id="f6c03-126">Requirement</span></span> | <span data-ttu-id="f6c03-127">值</span><span class="sxs-lookup"><span data-stu-id="f6c03-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c03-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f6c03-128">TAPI version</span></span><br/> | <span data-ttu-id="f6c03-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f6c03-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f6c03-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f6c03-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f6c03-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c03-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6c03-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f6c03-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f6c03-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f6c03-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f6c03-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c03-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6c03-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6c03-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

