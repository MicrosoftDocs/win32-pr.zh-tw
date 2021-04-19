---
description: Get \_ Item 方法會取得對應到指定之索引的 ITMedia 指標。
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'ITMediaCollection：： get_Item 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999416"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="e8572-103">ITMediaCollection：： get \_ Item 方法</span><span class="sxs-lookup"><span data-stu-id="e8572-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="e8572-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e8572-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e8572-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e8572-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e8572-106">**Get \_ Item** 方法會取得對應到指定之索引的 [**ITMedia**](itmedia.md)指標。</span><span class="sxs-lookup"><span data-stu-id="e8572-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8572-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8572-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e8572-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8572-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8572-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8572-110">要取得之媒體專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e8572-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="e8572-111">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e8572-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8572-112">所需專案的 [**ITMedia**](itmedia.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="e8572-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8572-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8572-113">Return value</span></span>

<span data-ttu-id="e8572-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e8572-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e8572-115">值</span><span class="sxs-lookup"><span data-stu-id="e8572-115">Value</span></span>                                                                                         | <span data-ttu-id="e8572-116">意義</span><span class="sxs-lookup"><span data-stu-id="e8572-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e8572-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e8572-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e8572-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e8572-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e8572-120">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="e8572-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="e8572-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e8572-122">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e8572-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="e8572-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e8572-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e8572-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e8572-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e8572-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8572-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e8572-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e8572-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="e8572-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e8572-129">備註</span><span class="sxs-lookup"><span data-stu-id="e8572-129">Remarks</span></span>

<span data-ttu-id="e8572-130">大部分 C 和 c + + 清單都是以0為基礎，但是此索引是以1為基礎，Visual Basic 相容性，這表示第一個專案的索引編號為1。</span><span class="sxs-lookup"><span data-stu-id="e8572-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8572-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8572-131">Requirements</span></span>



| <span data-ttu-id="e8572-132">需求</span><span class="sxs-lookup"><span data-stu-id="e8572-132">Requirement</span></span> | <span data-ttu-id="e8572-133">值</span><span class="sxs-lookup"><span data-stu-id="e8572-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8572-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e8572-134">TAPI version</span></span><br/> | <span data-ttu-id="e8572-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e8572-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e8572-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e8572-136">Header</span></span><br/>       | <dl> <span data-ttu-id="e8572-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8572-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8572-138">Library</span></span><br/>      | <dl> <span data-ttu-id="e8572-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e8572-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e8572-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="e8572-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8572-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8572-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8572-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8572-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="e8572-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="e8572-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="e8572-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




