---
description: ITSdp 介面提供 (SDP 的會話描述項通訊協定操作方法，請參閱 RFC 2327) 會議 blob 元件。
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: 'ITSdp 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978532"
---
# <a name="itsdp-interface"></a><span data-ttu-id="5e927-103">ITSdp 介面</span><span class="sxs-lookup"><span data-stu-id="5e927-103">ITSdp interface</span></span>

<span data-ttu-id="5e927-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="5e927-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5e927-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="5e927-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5e927-106">**ITSdp** 介面提供 (SDP 的會話描述項通訊協定操作方法，請參閱 RFC 2327) 會議 blob 元件。</span><span class="sxs-lookup"><span data-stu-id="5e927-106">The **ITSdp** interface provides methods for the manipulation of a Session Descriptor Protocol (SDP, see RFC 2327) conference blob component.</span></span> <span data-ttu-id="5e927-107">這個攔截器提供的功能包括：</span><span class="sxs-lookup"><span data-stu-id="5e927-107">It provides the following functionality:</span></span>

-   <span data-ttu-id="5e927-108">提供所有媒體通用屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="5e927-108">Provides access to some of the properties that are common to all the media.</span></span> <span data-ttu-id="5e927-109">這些內容包括與建立者的個人資訊、會話描述和網址類別型資訊有關的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e927-109">These include attributes pertaining to the creator's personal information, session description, and address type information.</span></span>
-   <span data-ttu-id="5e927-110">提供透過屬性存取時間和媒體集合的起點。</span><span class="sxs-lookup"><span data-stu-id="5e927-110">Provides the starting point for accessing the time and media collections through properties.</span></span>

<span data-ttu-id="5e927-111">**ITSdp** 介面是藉由在 [**ITConferenceBlob**](itconferenceblob.md)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="5e927-111">The **ITSdp** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="5e927-112">成員</span><span class="sxs-lookup"><span data-stu-id="5e927-112">Members</span></span>

<span data-ttu-id="5e927-113">**ITSdp** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="5e927-113">The **ITSdp** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5e927-114">**ITSdp** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5e927-114">**ITSdp** also has these types of members:</span></span>

-   [<span data-ttu-id="5e927-115">方法</span><span class="sxs-lookup"><span data-stu-id="5e927-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e927-116">方法</span><span class="sxs-lookup"><span data-stu-id="5e927-116">Methods</span></span>

<span data-ttu-id="5e927-117">**ITSdp** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5e927-117">The **ITSdp** interface has these methods.</span></span>



| <span data-ttu-id="5e927-118">方法</span><span class="sxs-lookup"><span data-stu-id="5e927-118">Method</span></span>                                                    | <span data-ttu-id="5e927-119">描述</span><span class="sxs-lookup"><span data-stu-id="5e927-119">Description</span></span>                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e927-120">**取得 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="5e927-120">**get\_Description**</span></span>](itsdp-get-description.md)         | <span data-ttu-id="5e927-121">取得會話描述。</span><span class="sxs-lookup"><span data-stu-id="5e927-121">Gets the session description.</span></span><br/>                                                            |
| [<span data-ttu-id="5e927-122">**取得 \_ IsValid**</span><span class="sxs-lookup"><span data-stu-id="5e927-122">**get\_IsValid**</span></span>](itsdp-get-isvalid.md)                 | <span data-ttu-id="5e927-123">驗證適用于結構和域值的 SDP blob。</span><span class="sxs-lookup"><span data-stu-id="5e927-123">Validates the SDP blob for structure and field values.</span></span><br/>                                   |
| [<span data-ttu-id="5e927-124">**取得 \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="5e927-124">**get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)   | <span data-ttu-id="5e927-125">取得來源主機的電腦位址。</span><span class="sxs-lookup"><span data-stu-id="5e927-125">Gets the machine address of the originating host.</span></span><br/>                                        |
| [<span data-ttu-id="5e927-126">**取得 \_ MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="5e927-126">**get\_MediaCollection**</span></span>](itsdp-get-mediacollection.md) | <span data-ttu-id="5e927-127">取得會議 [**ITMediaCollection**](itmediacollection.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5e927-127">Gets pointer to [**ITMediaCollection**](itmediacollection.md) interface for conference.</span></span><br/> |
| [<span data-ttu-id="5e927-128">**取得 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="5e927-128">**get\_Name**</span></span>](itsdp-get-name.md)                       | <span data-ttu-id="5e927-129">取得會話名稱。</span><span class="sxs-lookup"><span data-stu-id="5e927-129">Gets the session name.</span></span><br/>                                                                   |
| [<span data-ttu-id="5e927-130">**取得 \_ 建立者**</span><span class="sxs-lookup"><span data-stu-id="5e927-130">**get\_Originator**</span></span>](itsdp-get-originator.md)           | <span data-ttu-id="5e927-131">取得會議製作者。</span><span class="sxs-lookup"><span data-stu-id="5e927-131">Gets conference originator.</span></span><br/>                                                              |
| [<span data-ttu-id="5e927-132">**取得 \_ ProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="5e927-132">**get\_ProtocolVersion**</span></span>](itsdp-get-protocolversion.md) | <span data-ttu-id="5e927-133">取得 SDP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="5e927-133">Gets the SDP protocol version.</span></span><br/>                                                           |
| [<span data-ttu-id="5e927-134">**取得 \_ SessionId**</span><span class="sxs-lookup"><span data-stu-id="5e927-134">**get\_SessionId**</span></span>](itsdp-get-sessionid.md)             | <span data-ttu-id="5e927-135">取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e927-135">Gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span><br/> |
| [<span data-ttu-id="5e927-136">**取得 \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="5e927-136">**get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)   | <span data-ttu-id="5e927-137">取得32位 (理想的 NTP) 值，作為會話版本。</span><span class="sxs-lookup"><span data-stu-id="5e927-137">Gets the 32-bit (ideally NTP) value that serves as the session version.</span></span><br/>                  |
| [<span data-ttu-id="5e927-138">**取得 \_ TimeCollection**</span><span class="sxs-lookup"><span data-stu-id="5e927-138">**get\_TimeCollection**</span></span>](itsdp-get-timecollection.md)   | <span data-ttu-id="5e927-139">取得會議 [**ITTimeCollection**](ittimecollection.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5e927-139">Gets pointer to [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span><br/>   |
| [<span data-ttu-id="5e927-140">**取得 \_ Url**</span><span class="sxs-lookup"><span data-stu-id="5e927-140">**get\_Url**</span></span>](itsdp-get-url.md)                         | <span data-ttu-id="5e927-141">取得 URL。</span><span class="sxs-lookup"><span data-stu-id="5e927-141">Gets the URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="5e927-142">**GetEmailNames**</span><span class="sxs-lookup"><span data-stu-id="5e927-142">**GetEmailNames**</span></span>](itsdp-getemailnames.md)              | <span data-ttu-id="5e927-143">取得與會議 blob 相關聯的電子郵件名稱和位址陣列。</span><span class="sxs-lookup"><span data-stu-id="5e927-143">Gets array of e-mail names and addresses associated with conference blob.</span></span><br/>                |
| [<span data-ttu-id="5e927-144">**GetPhoneNumbers**</span><span class="sxs-lookup"><span data-stu-id="5e927-144">**GetPhoneNumbers**</span></span>](itsdp-getphonenumbers.md)          | <span data-ttu-id="5e927-145">取得電話號碼。</span><span class="sxs-lookup"><span data-stu-id="5e927-145">Gets the phone numbers.</span></span><br/>                                                                  |
| [<span data-ttu-id="5e927-146">**put \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="5e927-146">**put\_Description**</span></span>](itsdp-put-description.md)         | <span data-ttu-id="5e927-147">設定會話描述。</span><span class="sxs-lookup"><span data-stu-id="5e927-147">Sets the session description.</span></span><br/>                                                            |
| [<span data-ttu-id="5e927-148">**put \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="5e927-148">**put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)   | <span data-ttu-id="5e927-149">設定來源主機的電腦位址。</span><span class="sxs-lookup"><span data-stu-id="5e927-149">Sets the machine address of the originating host.</span></span><br/>                                        |
| [<span data-ttu-id="5e927-150">**put \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="5e927-150">**put\_Name**</span></span>](itsdp-put-name.md)                       | <span data-ttu-id="5e927-151">設定會話名稱。</span><span class="sxs-lookup"><span data-stu-id="5e927-151">Sets the session name.</span></span><br/>                                                                   |
| [<span data-ttu-id="5e927-152">**put \_ 建立者**</span><span class="sxs-lookup"><span data-stu-id="5e927-152">**put\_Originator**</span></span>](itsdp-put-originator.md)           | <span data-ttu-id="5e927-153">取得會議製作者。</span><span class="sxs-lookup"><span data-stu-id="5e927-153">Gets conference originator.</span></span><br/>                                                              |
| [<span data-ttu-id="5e927-154">**put \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="5e927-154">**put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)   | <span data-ttu-id="5e927-155">設定會話版本。</span><span class="sxs-lookup"><span data-stu-id="5e927-155">Sets session version.</span></span><br/>                                                                    |
| [<span data-ttu-id="5e927-156">**put \_ Url**</span><span class="sxs-lookup"><span data-stu-id="5e927-156">**put\_Url**</span></span>](itsdp-put-url.md)                         | <span data-ttu-id="5e927-157">設定 URL。</span><span class="sxs-lookup"><span data-stu-id="5e927-157">Sets the URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="5e927-158">**SetEmailNames**</span><span class="sxs-lookup"><span data-stu-id="5e927-158">**SetEmailNames**</span></span>](itsdp-setemailnames.md)              | <span data-ttu-id="5e927-159">設定與會議 blob 相關聯的電子郵件名稱和位址陣列。</span><span class="sxs-lookup"><span data-stu-id="5e927-159">Sets array of email names and addresses associated with conference blob.</span></span><br/>                 |
| [<span data-ttu-id="5e927-160">**SetPhoneNumbers**</span><span class="sxs-lookup"><span data-stu-id="5e927-160">**SetPhoneNumbers**</span></span>](itsdp-setphonenumbers.md)          | <span data-ttu-id="5e927-161">設定電話號碼。</span><span class="sxs-lookup"><span data-stu-id="5e927-161">Sets the phone numbers.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="5e927-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e927-162">Requirements</span></span>



| <span data-ttu-id="5e927-163">需求</span><span class="sxs-lookup"><span data-stu-id="5e927-163">Requirement</span></span> | <span data-ttu-id="5e927-164">值</span><span class="sxs-lookup"><span data-stu-id="5e927-164">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e927-165">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5e927-165">TAPI version</span></span><br/> | <span data-ttu-id="5e927-166">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5e927-166">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5e927-167">標頭</span><span class="sxs-lookup"><span data-stu-id="5e927-167">Header</span></span><br/>       | <dl> <span data-ttu-id="5e927-168"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e927-168"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e927-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e927-169">Library</span></span><br/>      | <dl> <span data-ttu-id="5e927-170"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="5e927-170"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5e927-171">DLL</span><span class="sxs-lookup"><span data-stu-id="5e927-171">DLL</span></span><br/>          | <dl> <span data-ttu-id="5e927-172"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e927-172"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

