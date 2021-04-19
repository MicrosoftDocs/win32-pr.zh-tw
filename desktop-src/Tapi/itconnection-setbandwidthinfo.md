---
description: SetBandwidthInfo 方法會設定頻寬資訊。
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection：： SetBandwidthInfo 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994645"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="75086-103">ITConnection：： SetBandwidthInfo 方法</span><span class="sxs-lookup"><span data-stu-id="75086-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="75086-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="75086-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="75086-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="75086-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="75086-106">**SetBandwidthInfo** 方法會設定頻寬資訊。</span><span class="sxs-lookup"><span data-stu-id="75086-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="75086-107">語法</span><span class="sxs-lookup"><span data-stu-id="75086-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="75086-108">參數</span><span class="sxs-lookup"><span data-stu-id="75086-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75086-109">*pModifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75086-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75086-110">指向表示所設定之頻寬範圍的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="75086-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="75086-111">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="75086-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="75086-112">*頻寬* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75086-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75086-113">頻寬。</span><span class="sxs-lookup"><span data-stu-id="75086-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75086-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="75086-114">Return value</span></span>

<span data-ttu-id="75086-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="75086-115">This method can return one of these values.</span></span>



| <span data-ttu-id="75086-116">值</span><span class="sxs-lookup"><span data-stu-id="75086-116">Value</span></span>                                                                                         | <span data-ttu-id="75086-117">意義</span><span class="sxs-lookup"><span data-stu-id="75086-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="75086-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="75086-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="75086-119">方法成功。</span><span class="sxs-lookup"><span data-stu-id="75086-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="75086-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75086-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="75086-121">*PModifier* 或 *頻寬* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="75086-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="75086-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="75086-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="75086-123">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="75086-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="75086-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="75086-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="75086-125">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="75086-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="75086-126"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="75086-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="75086-127">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="75086-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="75086-128">備註</span><span class="sxs-lookup"><span data-stu-id="75086-128">Remarks</span></span>

<span data-ttu-id="75086-129">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pModifier* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="75086-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="75086-130">參考： RFC 2327。</span><span class="sxs-lookup"><span data-stu-id="75086-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="75086-131">頻寬修飾詞通常會是 CT 或如下：</span><span class="sxs-lookup"><span data-stu-id="75086-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="75086-132">**CT 會議總計：** 每次在 Mbone 上或特定多播系統管理範圍區域內，會有一 [*次*](t-tapgloss.md) 隱含的最大頻寬關聯 (TTL)  (Mbone 頻寬與 TTL 限制在 Mbone 常見問題) 中提供。</span><span class="sxs-lookup"><span data-stu-id="75086-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="75086-133">如果會話或媒體的頻寬與範圍隱含的頻寬不同，則 \` b = CT： ... '應為會話提供行，以提供所使用之頻寬的上限。</span><span class="sxs-lookup"><span data-stu-id="75086-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="75086-134">這項功能的主要目的是要讓您大致瞭解兩個或多個會議是否可以同時並存。</span><span class="sxs-lookup"><span data-stu-id="75086-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="75086-135">**Application-Specific 最大值：** 頻寬會被視為應用程式特定的，也就是應用程式的最大頻寬概念。</span><span class="sxs-lookup"><span data-stu-id="75086-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="75086-136">一般來說，這會與應用程式的「最大頻寬」控制項上的設定相符（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="75086-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="75086-137">請注意，[CT] 會為所有網站上的所有媒體提供總頻寬圖。</span><span class="sxs-lookup"><span data-stu-id="75086-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="75086-138">在單一網站提供單一媒體的頻寬圖，雖然可能會同時傳送許多網站。</span><span class="sxs-lookup"><span data-stu-id="75086-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="75086-139">**延伸模組機制：** 工具寫入器可以定義實驗的頻寬修飾詞，方法是在其修飾詞前面加上 "X-"。</span><span class="sxs-lookup"><span data-stu-id="75086-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="75086-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="75086-140">Requirements</span></span>



| <span data-ttu-id="75086-141">需求</span><span class="sxs-lookup"><span data-stu-id="75086-141">Requirement</span></span> | <span data-ttu-id="75086-142">值</span><span class="sxs-lookup"><span data-stu-id="75086-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75086-143">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="75086-143">TAPI version</span></span><br/> | <span data-ttu-id="75086-144">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="75086-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="75086-145">標頭</span><span class="sxs-lookup"><span data-stu-id="75086-145">Header</span></span><br/>       | <dl> <span data-ttu-id="75086-146"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="75086-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="75086-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="75086-147">Library</span></span><br/>      | <dl> <span data-ttu-id="75086-148"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="75086-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="75086-149">DLL</span><span class="sxs-lookup"><span data-stu-id="75086-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="75086-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75086-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75086-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75086-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75086-152">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="75086-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

