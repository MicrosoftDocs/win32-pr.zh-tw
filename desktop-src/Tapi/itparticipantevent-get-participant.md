---
description: Get \_ 參與者方法會取得 ITParticipant 介面陣列的指標，代表牽涉到事件的參與者。
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'ITParticipantEvent：： get_Participant 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978751"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="f8ec6-103">ITParticipantEvent：： get \_ 參與者方法</span><span class="sxs-lookup"><span data-stu-id="f8ec6-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="f8ec6-104">\[**取得 \_參與者** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f8ec6-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f8ec6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f8ec6-106">**Get \_ 參與者** 方法會取得 [**ITParticipant**](itparticipant.md)介面陣列的指標，代表牽涉到事件的參與者。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ec6-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8ec6-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="f8ec6-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ec6-109">*ppParticipant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f8ec6-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ec6-110">[**ITParticipant**](itparticipant.md)介面陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ec6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ec6-111">Return value</span></span>

<span data-ttu-id="f8ec6-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f8ec6-113">值</span><span class="sxs-lookup"><span data-stu-id="f8ec6-113">Value</span></span>                                                                                           | <span data-ttu-id="f8ec6-114">意義</span><span class="sxs-lookup"><span data-stu-id="f8ec6-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8ec6-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="f8ec6-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f8ec6-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="f8ec6-118">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="f8ec6-119"><dt>**TAPI \_ E \_ NOITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="f8ec6-120">沒有與此事件相關聯的參與者。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="f8ec6-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="f8ec6-122">*PpParticipant* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="f8ec6-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f8ec6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ec6-123">Requirements</span></span>



| <span data-ttu-id="f8ec6-124">需求</span><span class="sxs-lookup"><span data-stu-id="f8ec6-124">Requirement</span></span> | <span data-ttu-id="f8ec6-125">值</span><span class="sxs-lookup"><span data-stu-id="f8ec6-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ec6-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f8ec6-126">TAPI version</span></span><br/> | <span data-ttu-id="f8ec6-127">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f8ec6-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f8ec6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f8ec6-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f8ec6-129"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ec6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8ec6-130">Library</span></span><br/>      | <dl> <span data-ttu-id="f8ec6-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f8ec6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8ec6-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="f8ec6-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8ec6-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f8ec6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8ec6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ec6-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="f8ec6-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="f8ec6-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f8ec6-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




