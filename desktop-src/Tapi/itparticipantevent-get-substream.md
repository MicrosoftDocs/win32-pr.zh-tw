---
description: 取得子串流會取得 \_ ITSubStream 介面陣列的指標，代表牽涉到事件的子串流。
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'ITParticipantEvent：： get_SubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994317"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="de4e6-103">ITParticipantEvent：：取得子 \_ 流方法</span><span class="sxs-lookup"><span data-stu-id="de4e6-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="de4e6-104">\[**取得 \_** 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中無法使用子串流。</span><span class="sxs-lookup"><span data-stu-id="de4e6-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="de4e6-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="de4e6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="de4e6-106">取得子串流會 **取得 \_** [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) 介面陣列的指標，代表牽涉到事件的子串流。</span><span class="sxs-lookup"><span data-stu-id="de4e6-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4e6-107">語法</span><span class="sxs-lookup"><span data-stu-id="de4e6-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="de4e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="de4e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4e6-109">*ppSubStream* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de4e6-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de4e6-110">[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)指標陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="de4e6-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4e6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de4e6-111">Return value</span></span>

<span data-ttu-id="de4e6-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="de4e6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="de4e6-113">值</span><span class="sxs-lookup"><span data-stu-id="de4e6-113">Value</span></span>                                                                                           | <span data-ttu-id="de4e6-114">意義</span><span class="sxs-lookup"><span data-stu-id="de4e6-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="de4e6-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="de4e6-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="de4e6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="de4e6-117"><dt>**TAPI \_ E \_ NOITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="de4e6-118">沒有與此事件相關聯的子串流。</span><span class="sxs-lookup"><span data-stu-id="de4e6-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="de4e6-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="de4e6-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="de4e6-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="de4e6-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="de4e6-122">*PpSubStream* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="de4e6-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="de4e6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="de4e6-123">Requirements</span></span>



| <span data-ttu-id="de4e6-124">需求</span><span class="sxs-lookup"><span data-stu-id="de4e6-124">Requirement</span></span> | <span data-ttu-id="de4e6-125">值</span><span class="sxs-lookup"><span data-stu-id="de4e6-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de4e6-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="de4e6-126">TAPI version</span></span><br/> | <span data-ttu-id="de4e6-127">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="de4e6-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="de4e6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="de4e6-128">Header</span></span><br/>       | <dl> <span data-ttu-id="de4e6-129"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="de4e6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="de4e6-130">Library</span></span><br/>      | <dl> <span data-ttu-id="de4e6-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="de4e6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="de4e6-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="de4e6-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de4e6-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="de4e6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de4e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4e6-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="de4e6-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="de4e6-136">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="de4e6-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

