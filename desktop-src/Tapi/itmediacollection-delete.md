---
description: Delete 方法會刪除對應至指定之索引的媒體。
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: 'ITMediaCollection：:D elete 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978772"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="2c78d-103">ITMediaCollection：:D elete 方法</span><span class="sxs-lookup"><span data-stu-id="2c78d-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="2c78d-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="2c78d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c78d-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2c78d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c78d-106">**Delete** 方法會刪除對應至指定之索引的媒體。</span><span class="sxs-lookup"><span data-stu-id="2c78d-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c78d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c78d-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="2c78d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c78d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c78d-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c78d-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c78d-110">要刪除之媒體的索引。</span><span class="sxs-lookup"><span data-stu-id="2c78d-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c78d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c78d-111">Return value</span></span>

<span data-ttu-id="2c78d-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2c78d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2c78d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2c78d-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="2c78d-114">Description</span><span class="sxs-lookup"><span data-stu-id="2c78d-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c78d-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="2c78d-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="2c78d-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="2c78d-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="2c78d-118">*索引* 參數的值小於1或大於目前的專案數目。</span><span class="sxs-lookup"><span data-stu-id="2c78d-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="2c78d-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="2c78d-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2c78d-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="2c78d-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="2c78d-122">內部錯誤 (只有在先前的呼叫傳回) 錯誤時才會發生。</span><span class="sxs-lookup"><span data-stu-id="2c78d-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="2c78d-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="2c78d-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="2c78d-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="2c78d-125"><dt>**\_錯誤碼中的 HRESULT \_ \_ (SDPBLB \_ 會議 \_ BLOB \_ 損毀)**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="2c78d-126">SDP blob 不存在。</span><span class="sxs-lookup"><span data-stu-id="2c78d-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="2c78d-127">備註</span><span class="sxs-lookup"><span data-stu-id="2c78d-127">Remarks</span></span>

<span data-ttu-id="2c78d-128">大部分 C 和 c + + 清單都是以0為基礎，但是此索引是以1為基礎，Visual Basic 相容性，這表示第一個專案的索引編號為1。</span><span class="sxs-lookup"><span data-stu-id="2c78d-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c78d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c78d-129">Requirements</span></span>



| <span data-ttu-id="2c78d-130">需求</span><span class="sxs-lookup"><span data-stu-id="2c78d-130">Requirement</span></span> | <span data-ttu-id="2c78d-131">值</span><span class="sxs-lookup"><span data-stu-id="2c78d-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c78d-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2c78d-132">TAPI version</span></span><br/> | <span data-ttu-id="2c78d-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2c78d-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2c78d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2c78d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="2c78d-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c78d-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c78d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="2c78d-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2c78d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c78d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="2c78d-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c78d-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c78d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c78d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c78d-141">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="2c78d-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




