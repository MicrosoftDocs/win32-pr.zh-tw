---
description: Delete 方法會刪除指定索引處的屬性。
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: 'ITAttributeList：:D elete 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991220"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="39638-103">ITAttributeList：:D elete 方法</span><span class="sxs-lookup"><span data-stu-id="39638-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="39638-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="39638-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="39638-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="39638-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="39638-106">**Delete** 方法會刪除指定索引處的屬性。</span><span class="sxs-lookup"><span data-stu-id="39638-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="39638-107">語法</span><span class="sxs-lookup"><span data-stu-id="39638-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="39638-108">參數</span><span class="sxs-lookup"><span data-stu-id="39638-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39638-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39638-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39638-110">要刪除之屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="39638-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39638-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="39638-111">Return value</span></span>

<span data-ttu-id="39638-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39638-112">This method can return one of these values.</span></span>



| <span data-ttu-id="39638-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="39638-113">Return code</span></span>                                                                                   | <span data-ttu-id="39638-114">Description</span><span class="sxs-lookup"><span data-stu-id="39638-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="39638-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="39638-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="39638-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="39638-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="39638-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="39638-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="39638-118">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="39638-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="39638-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="39638-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="39638-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="39638-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="39638-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="39638-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="39638-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="39638-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="39638-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="39638-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="39638-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="39638-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="39638-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="39638-125">Requirements</span></span>



| <span data-ttu-id="39638-126">需求</span><span class="sxs-lookup"><span data-stu-id="39638-126">Requirement</span></span> | <span data-ttu-id="39638-127">值</span><span class="sxs-lookup"><span data-stu-id="39638-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39638-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="39638-128">TAPI version</span></span><br/> | <span data-ttu-id="39638-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="39638-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="39638-130">標頭</span><span class="sxs-lookup"><span data-stu-id="39638-130">Header</span></span><br/>       | <dl> <span data-ttu-id="39638-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="39638-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="39638-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="39638-132">Library</span></span><br/>      | <dl> <span data-ttu-id="39638-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="39638-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="39638-134">DLL</span><span class="sxs-lookup"><span data-stu-id="39638-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="39638-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39638-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39638-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39638-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39638-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="39638-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




