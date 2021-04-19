---
description: Create 方法會使用預設屬性來建立新的媒體，然後將它新增至集合中指定的索引處，並傳回 ITMedia 介面的指標。
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection：： Create 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996485"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="4bfa7-103">ITMediaCollection：： Create 方法</span><span class="sxs-lookup"><span data-stu-id="4bfa7-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="4bfa7-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bfa7-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4bfa7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4bfa7-106">**Create** 方法會使用預設屬性來建立新的媒體，然後將它新增至集合中指定的索引處，並傳回 [**ITMedia**](itmedia.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfa7-107">語法</span><span class="sxs-lookup"><span data-stu-id="4bfa7-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="4bfa7-108">參數</span><span class="sxs-lookup"><span data-stu-id="4bfa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfa7-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bfa7-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bfa7-110">新專案的索引。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-110">Index for the new item.</span></span> <span data-ttu-id="4bfa7-111">索引的最小值是1，而索引的最大值是目前的專案數 + 1。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="4bfa7-112">*ppMedia* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4bfa7-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bfa7-113">已建立 [**ITMedia**](itmedia.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfa7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bfa7-114">Return value</span></span>

<span data-ttu-id="4bfa7-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4bfa7-116">值</span><span class="sxs-lookup"><span data-stu-id="4bfa7-116">Value</span></span>                                                                                         | <span data-ttu-id="4bfa7-117">意義</span><span class="sxs-lookup"><span data-stu-id="4bfa7-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4bfa7-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4bfa7-119">方法成功。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4bfa7-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4bfa7-121">*PpMedia* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="4bfa7-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4bfa7-123">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="4bfa7-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4bfa7-125">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4bfa7-126"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4bfa7-127">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4bfa7-128"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4bfa7-129">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4bfa7-130">備註</span><span class="sxs-lookup"><span data-stu-id="4bfa7-130">Remarks</span></span>

<span data-ttu-id="4bfa7-131">大部分 C 和 c + + 清單都是以0為基礎，但是此索引是以1為基礎，Visual Basic 相容性，這表示第一個專案的索引編號為1。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="4bfa7-132">TAPI 會在 **ITMediaCollection：： Create** 所傳回的 [**ITMedia**](itmedia.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="4bfa7-133">應用程式必須在 [**ITMedia**](itmedia.md)介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="4bfa7-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfa7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bfa7-134">Requirements</span></span>



| <span data-ttu-id="4bfa7-135">需求</span><span class="sxs-lookup"><span data-stu-id="4bfa7-135">Requirement</span></span> | <span data-ttu-id="4bfa7-136">值</span><span class="sxs-lookup"><span data-stu-id="4bfa7-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfa7-137">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4bfa7-137">TAPI version</span></span><br/> | <span data-ttu-id="4bfa7-138">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4bfa7-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4bfa7-139">標頭</span><span class="sxs-lookup"><span data-stu-id="4bfa7-139">Header</span></span><br/>       | <dl> <span data-ttu-id="4bfa7-140"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bfa7-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bfa7-141">Library</span></span><br/>      | <dl> <span data-ttu-id="4bfa7-142"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4bfa7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4bfa7-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="4bfa7-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa7-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfa7-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bfa7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfa7-146">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="4bfa7-147">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




