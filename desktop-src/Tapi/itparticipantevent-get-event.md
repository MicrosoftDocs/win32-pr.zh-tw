---
description: Get \_ 事件方法 \_ 會取得已發生之事件種類的參與者事件描述元。
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'ITParticipantEvent：： get_Event 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996454"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="7e9ee-103">ITParticipantEvent：： get \_ 事件方法</span><span class="sxs-lookup"><span data-stu-id="7e9ee-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="7e9ee-104">\[**取得 \_事件** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e9ee-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="7e9ee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e9ee-106">**Get \_ 事件** 方法會取得已發生之事件種類的 [**參與者 \_ 事件**](participant-event.md)描述元。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9ee-107">語法</span><span class="sxs-lookup"><span data-stu-id="7e9ee-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="7e9ee-108">參數</span><span class="sxs-lookup"><span data-stu-id="7e9ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e9ee-109">*pParticipantEvent* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7e9ee-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e9ee-110">事件 [**參與者 \_ 事件**](participant-event.md) 描述項的指標。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e9ee-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e9ee-111">Return value</span></span>

<span data-ttu-id="7e9ee-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7e9ee-113">值</span><span class="sxs-lookup"><span data-stu-id="7e9ee-113">Value</span></span>                                                                                         | <span data-ttu-id="7e9ee-114">意義</span><span class="sxs-lookup"><span data-stu-id="7e9ee-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e9ee-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7e9ee-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="7e9ee-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7e9ee-118">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="7e9ee-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7e9ee-120">*PParticipantEvent* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="7e9ee-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7e9ee-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e9ee-121">Requirements</span></span>



| <span data-ttu-id="7e9ee-122">需求</span><span class="sxs-lookup"><span data-stu-id="7e9ee-122">Requirement</span></span> | <span data-ttu-id="7e9ee-123">值</span><span class="sxs-lookup"><span data-stu-id="7e9ee-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9ee-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7e9ee-124">TAPI version</span></span><br/> | <span data-ttu-id="7e9ee-125">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7e9ee-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7e9ee-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7e9ee-126">Header</span></span><br/>       | <dl> <span data-ttu-id="7e9ee-127"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7e9ee-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e9ee-128">Library</span></span><br/>      | <dl> <span data-ttu-id="7e9ee-129"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7e9ee-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7e9ee-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="7e9ee-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ee-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7e9ee-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e9ee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9ee-133">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="7e9ee-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="7e9ee-134">**參與者 \_ 活動**</span><span class="sxs-lookup"><span data-stu-id="7e9ee-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




