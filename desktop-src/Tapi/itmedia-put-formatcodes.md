---
description: Put \_ FormatCodes 方法會設定媒體裝載格式的程式代碼清單。 Variant 包含 Bstr 的 SAFEARRAY。 該陣列中的每個 BSTR 都是格式的程式碼字串。
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia：:p ut_FormatCodes 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988235"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="0d8d5-105">ITMedia：:p 的 \_ FormatCodes 方法</span><span class="sxs-lookup"><span data-stu-id="0d8d5-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="0d8d5-106">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d8d5-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0d8d5-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d8d5-108">**Put \_ FormatCodes** 方法會設定媒體裝載格式的程式代碼清單。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="0d8d5-109">變數包含 **BSTR** s 的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="0d8d5-110">該陣列中的每個 **BSTR** 都是格式的程式碼字串。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8d5-111">語法</span><span class="sxs-lookup"><span data-stu-id="0d8d5-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="0d8d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="0d8d5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8d5-113">*NewVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d8d5-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8d5-114">媒體承載格式代碼的清單。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8d5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d8d5-115">Return value</span></span>

<span data-ttu-id="0d8d5-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0d8d5-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0d8d5-117">Return code</span></span>                                                                                   | <span data-ttu-id="0d8d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="0d8d5-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0d8d5-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0d8d5-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d8d5-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0d8d5-122">*NewVal* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="0d8d5-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d8d5-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0d8d5-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0d8d5-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0d8d5-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0d8d5-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0d8d5-129">備註</span><span class="sxs-lookup"><span data-stu-id="0d8d5-129">Remarks</span></span>

<span data-ttu-id="0d8d5-130">當提供承載格式的清單時，這表示這些格式可能會在會話中使用，但這些格式的第一種是會話的預設格式。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="0d8d5-131">當傳輸通訊協定為 RTP 時，格式代碼為 RTP 承載類型。</span><span class="sxs-lookup"><span data-stu-id="0d8d5-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d8d5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d8d5-132">Requirements</span></span>



| <span data-ttu-id="0d8d5-133">需求</span><span class="sxs-lookup"><span data-stu-id="0d8d5-133">Requirement</span></span> | <span data-ttu-id="0d8d5-134">值</span><span class="sxs-lookup"><span data-stu-id="0d8d5-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8d5-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0d8d5-135">TAPI version</span></span><br/> | <span data-ttu-id="0d8d5-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0d8d5-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0d8d5-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0d8d5-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0d8d5-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d8d5-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d8d5-139">Library</span></span><br/>      | <dl> <span data-ttu-id="0d8d5-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0d8d5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0d8d5-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="0d8d5-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d5-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8d5-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d8d5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8d5-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="0d8d5-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="0d8d5-145">**ITMedia：： get \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="0d8d5-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




