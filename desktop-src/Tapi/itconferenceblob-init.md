---
description: Init 方法會根據文字字串來初始化會議 blob。 如果 pBlob 為 Null，則會使用預設值。
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob：： Init 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990223"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="d3b2e-104">ITConferenceBlob：： Init 方法</span><span class="sxs-lookup"><span data-stu-id="d3b2e-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="d3b2e-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d3b2e-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d3b2e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d3b2e-107">**Init** 方法會根據文字字串來初始化會議 blob。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="d3b2e-108">如果 *pBlob* 為 **Null**，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b2e-109">語法</span><span class="sxs-lookup"><span data-stu-id="d3b2e-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d3b2e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3b2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b2e-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b2e-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b2e-112">會議名稱之 **BSTR** 表示的指標。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="d3b2e-113">*CharacterSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b2e-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b2e-114">[**BLOB \_字元集 \_ 的字元集**](blob-character-set.md) 描述元。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="d3b2e-115">*pBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b2e-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b2e-116">包含會議 blob 之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="d3b2e-117">如果是 **Null**，則會使用預設值來初始化會議 blob。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="d3b2e-118">目前，只有在 *CharacterSet* 參數設定為 [BCS ASCII] 時，才可以使用預設會議值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b2e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3b2e-119">Return value</span></span>

<span data-ttu-id="d3b2e-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-120">This method can return one of these values.</span></span>



| <span data-ttu-id="d3b2e-121">值</span><span class="sxs-lookup"><span data-stu-id="d3b2e-121">Value</span></span>                                                                                         | <span data-ttu-id="d3b2e-122">意義</span><span class="sxs-lookup"><span data-stu-id="d3b2e-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3b2e-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d3b2e-124">方法成功。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="d3b2e-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d3b2e-126">*PName*、 *CharacterSet* 或 *pBlob* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d3b2e-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d3b2e-128">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="d3b2e-129"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d3b2e-130">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d3b2e-131"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d3b2e-132">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="d3b2e-133">備註</span><span class="sxs-lookup"><span data-stu-id="d3b2e-133">Remarks</span></span>

<span data-ttu-id="d3b2e-134">如果 blob 已經初始化， **ITConferenceBlob：： Init** 將會傳回失敗。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="d3b2e-135">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 來配置 *pName* 和 *pBlob* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="d3b2e-136">當不再需要變數時，應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="d3b2e-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b2e-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3b2e-137">Requirements</span></span>



| <span data-ttu-id="d3b2e-138">需求</span><span class="sxs-lookup"><span data-stu-id="d3b2e-138">Requirement</span></span> | <span data-ttu-id="d3b2e-139">值</span><span class="sxs-lookup"><span data-stu-id="d3b2e-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b2e-140">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d3b2e-140">TAPI version</span></span><br/> | <span data-ttu-id="d3b2e-141">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d3b2e-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d3b2e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="d3b2e-142">Header</span></span><br/>       | <dl> <span data-ttu-id="d3b2e-143"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3b2e-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3b2e-144">Library</span></span><br/>      | <dl> <span data-ttu-id="d3b2e-145"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d3b2e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d3b2e-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="d3b2e-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2e-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b2e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3b2e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b2e-149">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="d3b2e-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="d3b2e-150">**BLOB \_ 字元集 \_**</span><span class="sxs-lookup"><span data-stu-id="d3b2e-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

