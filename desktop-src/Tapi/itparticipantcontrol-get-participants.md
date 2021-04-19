---
description: 取得 \_ 參與者方法會建立與目前會議相關聯的參與者集合。
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'ITParticipantControl：： get_Participants 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999209"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="3da0e-103">ITParticipantControl：：取得 \_ 參與者方法</span><span class="sxs-lookup"><span data-stu-id="3da0e-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="3da0e-104">\[**取得 \_參與者** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="3da0e-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3da0e-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="3da0e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3da0e-106">**取得 \_ 參與者** 方法會建立與目前會議相關聯的參與者集合。</span><span class="sxs-lookup"><span data-stu-id="3da0e-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="3da0e-107">這個方法是針對 Automation 用戶端應用程式所提供，例如以 Visual Basic 撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3da0e-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="3da0e-108">C 和 c + + 應用程式必須使用 [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3da0e-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da0e-109">語法</span><span class="sxs-lookup"><span data-stu-id="3da0e-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="3da0e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3da0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da0e-111">*pVariant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3da0e-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da0e-112">**VARIANT** 的指標，其中包含 [**ITParticipant**](itparticipant.md)介面指標的 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。</span><span class="sxs-lookup"><span data-stu-id="3da0e-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da0e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3da0e-113">Return value</span></span>

<span data-ttu-id="3da0e-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3da0e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3da0e-115">值</span><span class="sxs-lookup"><span data-stu-id="3da0e-115">Value</span></span>                                                                                         | <span data-ttu-id="3da0e-116">意義</span><span class="sxs-lookup"><span data-stu-id="3da0e-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3da0e-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3da0e-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="3da0e-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3da0e-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3da0e-120">*PVariant* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="3da0e-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="3da0e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3da0e-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3da0e-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3da0e-123">備註</span><span class="sxs-lookup"><span data-stu-id="3da0e-123">Remarks</span></span>

<span data-ttu-id="3da0e-124">TAPI 會在 **ITParticipantControl：： get \_ 參與者** 所傳回的 [**ITParticipant**](itparticipant.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="3da0e-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="3da0e-125">應用程式必須在 **ITParticipant** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="3da0e-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da0e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3da0e-126">Requirements</span></span>



| <span data-ttu-id="3da0e-127">需求</span><span class="sxs-lookup"><span data-stu-id="3da0e-127">Requirement</span></span> | <span data-ttu-id="3da0e-128">值</span><span class="sxs-lookup"><span data-stu-id="3da0e-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3da0e-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3da0e-129">TAPI version</span></span><br/> | <span data-ttu-id="3da0e-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3da0e-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3da0e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3da0e-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3da0e-132"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="3da0e-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="3da0e-133">Library</span></span><br/>      | <dl> <span data-ttu-id="3da0e-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3da0e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3da0e-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="3da0e-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da0e-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3da0e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3da0e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da0e-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="3da0e-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="3da0e-139">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="3da0e-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="3da0e-140">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="3da0e-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="3da0e-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="3da0e-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




