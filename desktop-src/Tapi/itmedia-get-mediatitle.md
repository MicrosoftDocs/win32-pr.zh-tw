---
description: Get \_ MediaTitle 方法會抓取媒體的文字標題，讓應用程式用來提供資訊或顯示用途。 如果字元集是 ASCII，則這必須是 ASCII 可轉換字串。 否則，它可以是任何 BSTR 字串。
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'ITMedia：： get_MediaTitle 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989812"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="37280-105">ITMedia：： get \_ MediaTitle 方法</span><span class="sxs-lookup"><span data-stu-id="37280-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="37280-106">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="37280-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37280-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="37280-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="37280-108">**Get \_ MediaTitle** 方法會抓取媒體的文字標題，讓應用程式用來提供資訊或顯示用途。</span><span class="sxs-lookup"><span data-stu-id="37280-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="37280-109">如果字元集是 ASCII，則這必須是 ASCII 可轉換字串。</span><span class="sxs-lookup"><span data-stu-id="37280-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="37280-110">否則，它可以是任何 **BSTR** 字串。</span><span class="sxs-lookup"><span data-stu-id="37280-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="37280-111">語法</span><span class="sxs-lookup"><span data-stu-id="37280-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="37280-112">參數</span><span class="sxs-lookup"><span data-stu-id="37280-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37280-113">*ppMediaTitle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37280-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37280-114">包含媒體標題之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="37280-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37280-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="37280-115">Return value</span></span>

<span data-ttu-id="37280-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="37280-116">This method can return one of these values.</span></span>



| <span data-ttu-id="37280-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="37280-117">Return code</span></span>                                                                                   | <span data-ttu-id="37280-118">Description</span><span class="sxs-lookup"><span data-stu-id="37280-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="37280-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="37280-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="37280-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="37280-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="37280-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="37280-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="37280-122">*PpMediaTitle* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="37280-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="37280-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="37280-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="37280-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="37280-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="37280-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="37280-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="37280-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="37280-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="37280-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="37280-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="37280-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="37280-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="37280-129">備註</span><span class="sxs-lookup"><span data-stu-id="37280-129">Remarks</span></span>

<span data-ttu-id="37280-130">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppMediaTitle* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="37280-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="37280-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="37280-131">Requirements</span></span>



| <span data-ttu-id="37280-132">需求</span><span class="sxs-lookup"><span data-stu-id="37280-132">Requirement</span></span> | <span data-ttu-id="37280-133">值</span><span class="sxs-lookup"><span data-stu-id="37280-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37280-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="37280-134">TAPI version</span></span><br/> | <span data-ttu-id="37280-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="37280-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="37280-136">標頭</span><span class="sxs-lookup"><span data-stu-id="37280-136">Header</span></span><br/>       | <dl> <span data-ttu-id="37280-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="37280-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="37280-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="37280-138">Library</span></span><br/>      | <dl> <span data-ttu-id="37280-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="37280-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="37280-140">DLL</span><span class="sxs-lookup"><span data-stu-id="37280-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="37280-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37280-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37280-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37280-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37280-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="37280-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="37280-144">**ITMedia：:P 的 \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="37280-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

