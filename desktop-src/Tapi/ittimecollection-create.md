---
description: Create 方法會建立新的 ITTime 元件。
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'ITTimeCollection：： Create 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982986"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="fad3c-103">ITTimeCollection：： Create 方法</span><span class="sxs-lookup"><span data-stu-id="fad3c-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="fad3c-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="fad3c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fad3c-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fad3c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fad3c-106">**Create** 方法會建立新的 [**ITTime**](ittime.md)元件。</span><span class="sxs-lookup"><span data-stu-id="fad3c-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad3c-107">語法</span><span class="sxs-lookup"><span data-stu-id="fad3c-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="fad3c-108">參數</span><span class="sxs-lookup"><span data-stu-id="fad3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad3c-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fad3c-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad3c-110">要建立之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="fad3c-110">Index of the item to create.</span></span> <span data-ttu-id="fad3c-111"> (索引陣列是以一為基礎的 ) 。</span><span class="sxs-lookup"><span data-stu-id="fad3c-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="fad3c-112">*ppTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fad3c-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fad3c-113">所建立 b 元件的指標。</span><span class="sxs-lookup"><span data-stu-id="fad3c-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad3c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fad3c-114">Return value</span></span>

<span data-ttu-id="fad3c-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fad3c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fad3c-116">值</span><span class="sxs-lookup"><span data-stu-id="fad3c-116">Value</span></span>                                                                                         | <span data-ttu-id="fad3c-117">意義</span><span class="sxs-lookup"><span data-stu-id="fad3c-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fad3c-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fad3c-119">方法成功。</span><span class="sxs-lookup"><span data-stu-id="fad3c-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fad3c-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fad3c-121">*PpTime* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="fad3c-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="fad3c-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fad3c-123">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="fad3c-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="fad3c-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fad3c-125">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="fad3c-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fad3c-126"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fad3c-127">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fad3c-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fad3c-128"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fad3c-129">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="fad3c-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fad3c-130">備註</span><span class="sxs-lookup"><span data-stu-id="fad3c-130">Remarks</span></span>

<span data-ttu-id="fad3c-131">TAPI 會在 **ITTimeCollection：： Create** 所傳回的 [**ITTime**](ittime.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="fad3c-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="fad3c-132">應用程式必須在 v 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="fad3c-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="fad3c-133">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="fad3c-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="fad3c-134">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="fad3c-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad3c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fad3c-135">Requirements</span></span>



| <span data-ttu-id="fad3c-136">需求</span><span class="sxs-lookup"><span data-stu-id="fad3c-136">Requirement</span></span> | <span data-ttu-id="fad3c-137">值</span><span class="sxs-lookup"><span data-stu-id="fad3c-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fad3c-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fad3c-138">TAPI version</span></span><br/> | <span data-ttu-id="fad3c-139">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fad3c-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fad3c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fad3c-140">Header</span></span><br/>       | <dl> <span data-ttu-id="fad3c-141"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fad3c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="fad3c-142">Library</span></span><br/>      | <dl> <span data-ttu-id="fad3c-143"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fad3c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fad3c-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="fad3c-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad3c-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad3c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fad3c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad3c-147">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="fad3c-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="fad3c-148">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="fad3c-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




