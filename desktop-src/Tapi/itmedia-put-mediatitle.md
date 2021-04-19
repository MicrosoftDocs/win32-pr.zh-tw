---
description: Put \_ MediaTitle 方法會設定媒體的文字標題，讓應用程式用來提供資訊或顯示用途。 如果字元集是 ASCII，則這必須是 ASCII 可轉換字串。 否則，它可以是任何 BSTR 字串。
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia：:p ut_MediaTitle 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990564"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="9a79e-105">ITMedia：:p 的 \_ MediaTitle 方法</span><span class="sxs-lookup"><span data-stu-id="9a79e-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="9a79e-106">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="9a79e-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a79e-107">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9a79e-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9a79e-108">**Put \_ MediaTitle** 方法會設定媒體的文字標題，讓應用程式用來提供資訊或顯示用途。</span><span class="sxs-lookup"><span data-stu-id="9a79e-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="9a79e-109">如果字元集是 ASCII，則這必須是 ASCII 可轉換字串。</span><span class="sxs-lookup"><span data-stu-id="9a79e-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="9a79e-110">否則，它可以是任何 **BSTR** 字串。</span><span class="sxs-lookup"><span data-stu-id="9a79e-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a79e-111">語法</span><span class="sxs-lookup"><span data-stu-id="9a79e-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="9a79e-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a79e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a79e-113">*pMediaTitle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a79e-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a79e-114">包含媒體標題之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="9a79e-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a79e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a79e-115">Return value</span></span>

<span data-ttu-id="9a79e-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9a79e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9a79e-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a79e-117">Return code</span></span>                                                                                   | <span data-ttu-id="9a79e-118">Description</span><span class="sxs-lookup"><span data-stu-id="9a79e-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9a79e-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a79e-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="9a79e-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9a79e-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9a79e-122">*PMediaTitle* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="9a79e-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="9a79e-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9a79e-124">*PMediaTitle* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="9a79e-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="9a79e-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a79e-126">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="9a79e-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9a79e-127"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9a79e-128">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a79e-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9a79e-129"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9a79e-130">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="9a79e-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9a79e-131">備註</span><span class="sxs-lookup"><span data-stu-id="9a79e-131">Remarks</span></span>

<span data-ttu-id="9a79e-132">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pMediaTitle* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="9a79e-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="9a79e-133">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="9a79e-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="9a79e-134">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="9a79e-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a79e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a79e-135">Requirements</span></span>



| <span data-ttu-id="9a79e-136">需求</span><span class="sxs-lookup"><span data-stu-id="9a79e-136">Requirement</span></span> | <span data-ttu-id="9a79e-137">值</span><span class="sxs-lookup"><span data-stu-id="9a79e-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a79e-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9a79e-138">TAPI version</span></span><br/> | <span data-ttu-id="9a79e-139">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9a79e-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9a79e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9a79e-140">Header</span></span><br/>       | <dl> <span data-ttu-id="9a79e-141"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a79e-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a79e-142">Library</span></span><br/>      | <dl> <span data-ttu-id="9a79e-143"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9a79e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9a79e-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="9a79e-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a79e-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a79e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a79e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a79e-147">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="9a79e-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="9a79e-148">**ITMedia：： get \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="9a79e-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

