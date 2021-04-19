---
description: Delete 方法會刪除 ITTime 元件。
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: 'ITTimeCollection：:D elete 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987060"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="074f8-103">ITTimeCollection：:D elete 方法</span><span class="sxs-lookup"><span data-stu-id="074f8-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="074f8-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="074f8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="074f8-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="074f8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="074f8-106">**Delete** 方法會刪除 [**ITTime**](ittime.md)元件。</span><span class="sxs-lookup"><span data-stu-id="074f8-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="074f8-107">語法</span><span class="sxs-lookup"><span data-stu-id="074f8-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="074f8-108">參數</span><span class="sxs-lookup"><span data-stu-id="074f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074f8-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="074f8-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074f8-110">要刪除之 [**ITTime**](ittime.md) 元件的索引。</span><span class="sxs-lookup"><span data-stu-id="074f8-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="074f8-111"> (索引陣列是以一為基礎的 ) 。</span><span class="sxs-lookup"><span data-stu-id="074f8-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074f8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="074f8-112">Return value</span></span>

<span data-ttu-id="074f8-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="074f8-113">This method can return one of these values.</span></span>



| <span data-ttu-id="074f8-114">值</span><span class="sxs-lookup"><span data-stu-id="074f8-114">Value</span></span>                                                                                         | <span data-ttu-id="074f8-115">意義</span><span class="sxs-lookup"><span data-stu-id="074f8-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="074f8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="074f8-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="074f8-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="074f8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="074f8-119">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="074f8-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="074f8-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="074f8-121">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="074f8-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="074f8-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="074f8-123">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="074f8-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="074f8-124"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="074f8-125">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="074f8-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="074f8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="074f8-126">Requirements</span></span>



| <span data-ttu-id="074f8-127">需求</span><span class="sxs-lookup"><span data-stu-id="074f8-127">Requirement</span></span> | <span data-ttu-id="074f8-128">值</span><span class="sxs-lookup"><span data-stu-id="074f8-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="074f8-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="074f8-129">TAPI version</span></span><br/> | <span data-ttu-id="074f8-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="074f8-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="074f8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="074f8-131">Header</span></span><br/>       | <dl> <span data-ttu-id="074f8-132"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="074f8-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="074f8-133">Library</span></span><br/>      | <dl> <span data-ttu-id="074f8-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="074f8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="074f8-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="074f8-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074f8-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074f8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="074f8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074f8-138">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="074f8-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="074f8-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="074f8-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




