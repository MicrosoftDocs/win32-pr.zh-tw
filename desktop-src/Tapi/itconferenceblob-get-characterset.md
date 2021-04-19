---
description: Get \_ CharacterSet 方法會取得 \_ \_ 目前會議 blob 中所使用之字元集的 BLOB 字元集描述元。
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'ITConferenceBlob：： get_CharacterSet 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984068"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="3695c-103">ITConferenceBlob：： get \_ CharacterSet 方法</span><span class="sxs-lookup"><span data-stu-id="3695c-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="3695c-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="3695c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3695c-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="3695c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3695c-106">**Get \_ CharacterSet** 方法會取得目前會議 blob 中所使用之字元集的 [**BLOB \_ 字元集 \_**](blob-character-set.md)描述元。</span><span class="sxs-lookup"><span data-stu-id="3695c-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="3695c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3695c-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="3695c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3695c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3695c-109">*pCharacterSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3695c-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3695c-110">字元集的 [**BLOB \_ 字元集 \_**](blob-character-set.md) 描述元指標。</span><span class="sxs-lookup"><span data-stu-id="3695c-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3695c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3695c-111">Return value</span></span>

<span data-ttu-id="3695c-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3695c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3695c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3695c-113">Return code</span></span>                                                                                                   | <span data-ttu-id="3695c-114">Description</span><span class="sxs-lookup"><span data-stu-id="3695c-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="3695c-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="3695c-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="3695c-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3695c-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="3695c-118">*PCharacterSet* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="3695c-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="3695c-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="3695c-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3695c-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="3695c-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="3695c-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3695c-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3695c-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="3695c-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="3695c-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="3695c-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="3695c-126">*pCharacterSet* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3695c-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="3695c-127"><dt>**(HRESULT) 錯誤 \_ 的 \_ 資料無效**</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="3695c-128">目前的字元集無效或無法使用。</span><span class="sxs-lookup"><span data-stu-id="3695c-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="3695c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3695c-129">Requirements</span></span>



| <span data-ttu-id="3695c-130">需求</span><span class="sxs-lookup"><span data-stu-id="3695c-130">Requirement</span></span> | <span data-ttu-id="3695c-131">值</span><span class="sxs-lookup"><span data-stu-id="3695c-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3695c-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3695c-132">TAPI version</span></span><br/> | <span data-ttu-id="3695c-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3695c-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3695c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="3695c-134">Header</span></span><br/>       | <dl> <span data-ttu-id="3695c-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3695c-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="3695c-136">Library</span></span><br/>      | <dl> <span data-ttu-id="3695c-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3695c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3695c-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="3695c-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3695c-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3695c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3695c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3695c-141">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="3695c-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="3695c-142">**BLOB \_ 字元集 \_**</span><span class="sxs-lookup"><span data-stu-id="3695c-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




