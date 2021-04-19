---
description: Put \_ AttributeList 方法會設定屬性清單。
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'ITAttributeList：:p ut_AttributeList 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983205"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="b7e72-103">ITAttributeList：:p 的 \_ AttributeList 方法</span><span class="sxs-lookup"><span data-stu-id="b7e72-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="b7e72-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="b7e72-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b7e72-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b7e72-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b7e72-106">**Put \_ AttributeList** 方法會設定屬性清單。</span><span class="sxs-lookup"><span data-stu-id="b7e72-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e72-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7e72-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b7e72-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7e72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e72-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7e72-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e72-110">要設定的屬性陣列。</span><span class="sxs-lookup"><span data-stu-id="b7e72-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e72-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7e72-111">Return value</span></span>

<span data-ttu-id="b7e72-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b7e72-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b7e72-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b7e72-113">Return code</span></span>                                                                                   | <span data-ttu-id="b7e72-114">Description</span><span class="sxs-lookup"><span data-stu-id="b7e72-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b7e72-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b7e72-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="b7e72-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b7e72-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b7e72-118">*NewVal* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="b7e72-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="b7e72-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b7e72-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b7e72-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b7e72-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b7e72-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7e72-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b7e72-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b7e72-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="b7e72-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b7e72-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7e72-125">Requirements</span></span>



| <span data-ttu-id="b7e72-126">需求</span><span class="sxs-lookup"><span data-stu-id="b7e72-126">Requirement</span></span> | <span data-ttu-id="b7e72-127">值</span><span class="sxs-lookup"><span data-stu-id="b7e72-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e72-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b7e72-128">TAPI version</span></span><br/> | <span data-ttu-id="b7e72-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b7e72-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b7e72-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b7e72-130">Header</span></span><br/>       | <dl> <span data-ttu-id="b7e72-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7e72-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7e72-132">Library</span></span><br/>      | <dl> <span data-ttu-id="b7e72-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b7e72-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e72-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="b7e72-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e72-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e72-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7e72-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e72-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="b7e72-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="b7e72-138">**ITAttributeList：： get \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="b7e72-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




