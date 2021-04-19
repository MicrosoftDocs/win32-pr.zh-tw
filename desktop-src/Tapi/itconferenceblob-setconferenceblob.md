---
description: SetConferenceBlob 方法會認可會議 blob 的變更。 若要第一次初始化會議 blob，請改用 Init 方法。
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'ITConferenceBlob：： SetConferenceBlob 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001574"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="410b7-104">ITConferenceBlob：： SetConferenceBlob 方法</span><span class="sxs-lookup"><span data-stu-id="410b7-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="410b7-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="410b7-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="410b7-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="410b7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="410b7-107">**SetConferenceBlob** 方法會認可會議 blob 的變更。</span><span class="sxs-lookup"><span data-stu-id="410b7-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="410b7-108">若要第一次初始化會議 blob，請改用 [**Init**](itconferenceblob-init.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="410b7-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="410b7-109">語法</span><span class="sxs-lookup"><span data-stu-id="410b7-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="410b7-110">參數</span><span class="sxs-lookup"><span data-stu-id="410b7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="410b7-111">*CharacterSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="410b7-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410b7-112">[**BLOB \_會議 \_**](blob-character-set.md) blob 字元集的字元集描述項。</span><span class="sxs-lookup"><span data-stu-id="410b7-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="410b7-113">*pBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="410b7-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410b7-114">包含會議 blob 之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="410b7-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="410b7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="410b7-115">Return value</span></span>

<span data-ttu-id="410b7-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="410b7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="410b7-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="410b7-117">Return code</span></span>                                                                                   | <span data-ttu-id="410b7-118">Description</span><span class="sxs-lookup"><span data-stu-id="410b7-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="410b7-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="410b7-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="410b7-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="410b7-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="410b7-122">*CharacterSet* 或 *pBlob* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="410b7-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="410b7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="410b7-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="410b7-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="410b7-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="410b7-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="410b7-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="410b7-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="410b7-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="410b7-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="410b7-129">備註</span><span class="sxs-lookup"><span data-stu-id="410b7-129">Remarks</span></span>

<span data-ttu-id="410b7-130">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pBlob* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="410b7-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="410b7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="410b7-131">Requirements</span></span>



| <span data-ttu-id="410b7-132">需求</span><span class="sxs-lookup"><span data-stu-id="410b7-132">Requirement</span></span> | <span data-ttu-id="410b7-133">值</span><span class="sxs-lookup"><span data-stu-id="410b7-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="410b7-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="410b7-134">TAPI version</span></span><br/> | <span data-ttu-id="410b7-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="410b7-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="410b7-136">標頭</span><span class="sxs-lookup"><span data-stu-id="410b7-136">Header</span></span><br/>       | <dl> <span data-ttu-id="410b7-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="410b7-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="410b7-138">Library</span></span><br/>      | <dl> <span data-ttu-id="410b7-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="410b7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="410b7-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="410b7-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="410b7-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410b7-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="410b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410b7-143">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="410b7-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="410b7-144">**BLOB \_ 字元集 \_**</span><span class="sxs-lookup"><span data-stu-id="410b7-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

