---
description: EnumerateParticipants 方法會列舉與目前會議相關聯的參與者。
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl：： EnumerateParticipants 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988655"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="c1fc2-103">ITParticipantControl：： EnumerateParticipants 方法</span><span class="sxs-lookup"><span data-stu-id="c1fc2-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="c1fc2-104">\[**EnumerateParticipants** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1fc2-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c1fc2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c1fc2-106">**EnumerateParticipants** 方法會列舉與目前會議相關聯的參與者。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="c1fc2-107">這個方法是針對 C 和 c + + 應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="c1fc2-108">Automation 用戶端應用程式（例如以 Visual Basic 撰寫的應用程式）必須使用 [**取得 \_ 參與者**](itparticipantcontrol-get-participants.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fc2-109">語法</span><span class="sxs-lookup"><span data-stu-id="c1fc2-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="c1fc2-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1fc2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fc2-111">*ppEnumParticipants* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1fc2-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fc2-112">[**IEnumParticipant**](ienumparticipant.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fc2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1fc2-113">Return value</span></span>

<span data-ttu-id="c1fc2-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c1fc2-115">值</span><span class="sxs-lookup"><span data-stu-id="c1fc2-115">Value</span></span>                                                                                         | <span data-ttu-id="c1fc2-116">意義</span><span class="sxs-lookup"><span data-stu-id="c1fc2-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1fc2-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1fc2-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c1fc2-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1fc2-120">*PpEnumParticipants* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="c1fc2-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1fc2-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="c1fc2-123">備註</span><span class="sxs-lookup"><span data-stu-id="c1fc2-123">Remarks</span></span>

<span data-ttu-id="c1fc2-124">TAPI 會在 **ITParticipantControl：： EnumerateParticipants** 傳回的 [**IEnumParticipant**](ienumparticipant.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="c1fc2-125">應用程式必須在 **IEnumParticipant** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c1fc2-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fc2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1fc2-126">Requirements</span></span>



| <span data-ttu-id="c1fc2-127">需求</span><span class="sxs-lookup"><span data-stu-id="c1fc2-127">Requirement</span></span> | <span data-ttu-id="c1fc2-128">值</span><span class="sxs-lookup"><span data-stu-id="c1fc2-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fc2-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c1fc2-129">TAPI version</span></span><br/> | <span data-ttu-id="c1fc2-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1fc2-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c1fc2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c1fc2-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c1fc2-132"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c1fc2-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1fc2-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c1fc2-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c1fc2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c1fc2-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c1fc2-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1fc2-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c1fc2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1fc2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fc2-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="c1fc2-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="c1fc2-139">**取得 \_ 參與者**</span><span class="sxs-lookup"><span data-stu-id="c1fc2-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="c1fc2-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="c1fc2-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="c1fc2-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c1fc2-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




