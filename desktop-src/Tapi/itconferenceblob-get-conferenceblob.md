---
description: Get \_ ConferenceBlob 方法會取得目前儲存在會議 blob 物件中之文字會議 blob 的指標。
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'ITConferenceBlob：： get_ConferenceBlob 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995307"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="8af3f-103">ITConferenceBlob：： get \_ ConferenceBlob 方法</span><span class="sxs-lookup"><span data-stu-id="8af3f-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="8af3f-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="8af3f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8af3f-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8af3f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8af3f-106">**Get \_ ConferenceBlob** 方法會取得目前儲存在會議 blob 物件中之文字會議 blob 的指標。</span><span class="sxs-lookup"><span data-stu-id="8af3f-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af3f-107">語法</span><span class="sxs-lookup"><span data-stu-id="8af3f-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8af3f-108">參數</span><span class="sxs-lookup"><span data-stu-id="8af3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af3f-109">*ppBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8af3f-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8af3f-110">包含會議 blob 之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="8af3f-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af3f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8af3f-111">Return value</span></span>

<span data-ttu-id="8af3f-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8af3f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8af3f-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8af3f-113">Return code</span></span>                                                                                   | <span data-ttu-id="8af3f-114">Description</span><span class="sxs-lookup"><span data-stu-id="8af3f-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8af3f-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8af3f-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="8af3f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8af3f-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8af3f-118">*PpBlob* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="8af3f-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8af3f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8af3f-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8af3f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8af3f-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8af3f-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8af3f-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8af3f-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8af3f-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="8af3f-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8af3f-125">備註</span><span class="sxs-lookup"><span data-stu-id="8af3f-125">Remarks</span></span>

<span data-ttu-id="8af3f-126">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppBlob* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8af3f-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af3f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8af3f-127">Requirements</span></span>



| <span data-ttu-id="8af3f-128">需求</span><span class="sxs-lookup"><span data-stu-id="8af3f-128">Requirement</span></span> | <span data-ttu-id="8af3f-129">值</span><span class="sxs-lookup"><span data-stu-id="8af3f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8af3f-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8af3f-130">TAPI version</span></span><br/> | <span data-ttu-id="8af3f-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8af3f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8af3f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8af3f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8af3f-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8af3f-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="8af3f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8af3f-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8af3f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8af3f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8af3f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af3f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af3f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8af3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af3f-139">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="8af3f-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="8af3f-140">**BLOB \_ 字元集 \_**</span><span class="sxs-lookup"><span data-stu-id="8af3f-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

