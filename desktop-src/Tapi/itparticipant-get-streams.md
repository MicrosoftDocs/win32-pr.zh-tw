---
description: 取得 \_ 資料流程方法會建立與目前參與者相關聯的資料流程集合。
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'ITParticipant：： get_Streams 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987117"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="c0ad3-103">ITParticipant：： get \_ 串流方法</span><span class="sxs-lookup"><span data-stu-id="c0ad3-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="c0ad3-104">\[**取得 \_資料流程** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0ad3-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c0ad3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0ad3-106">**取得 \_ 資料流程** 方法會建立與目前參與者相關聯的資料流程集合。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="c0ad3-107">這個方法是針對 Automation 用戶端應用程式所提供，例如以 Visual Basic 撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="c0ad3-108">C 和 c + + 應用程式必須使用 [**EnumerateStreams**](itparticipant-enumeratestreams.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ad3-109">語法</span><span class="sxs-lookup"><span data-stu-id="c0ad3-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="c0ad3-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0ad3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ad3-111">*pVariant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0ad3-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad3-112">**VARIANT** 的指標，其中包含 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面指標的 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ad3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0ad3-113">Return value</span></span>

<span data-ttu-id="c0ad3-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c0ad3-115">值</span><span class="sxs-lookup"><span data-stu-id="c0ad3-115">Value</span></span>                                                                                         | <span data-ttu-id="c0ad3-116">意義</span><span class="sxs-lookup"><span data-stu-id="c0ad3-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c0ad3-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c0ad3-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c0ad3-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c0ad3-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c0ad3-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c0ad3-122">*PVariant* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c0ad3-123">備註</span><span class="sxs-lookup"><span data-stu-id="c0ad3-123">Remarks</span></span>

<span data-ttu-id="c0ad3-124">TAPI 會在 **ITParticipant：： get \_ 資料流程** 所傳回的 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="c0ad3-125">應用程式必須在 **ITStream** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c0ad3-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ad3-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0ad3-126">Requirements</span></span>



| <span data-ttu-id="c0ad3-127">需求</span><span class="sxs-lookup"><span data-stu-id="c0ad3-127">Requirement</span></span> | <span data-ttu-id="c0ad3-128">值</span><span class="sxs-lookup"><span data-stu-id="c0ad3-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ad3-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c0ad3-129">TAPI version</span></span><br/> | <span data-ttu-id="c0ad3-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c0ad3-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="c0ad3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c0ad3-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c0ad3-132"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0ad3-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c0ad3-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c0ad3-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c0ad3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ad3-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c0ad3-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad3-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ad3-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0ad3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ad3-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c0ad3-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="c0ad3-139">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="c0ad3-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="c0ad3-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="c0ad3-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="c0ad3-141">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="c0ad3-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="c0ad3-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c0ad3-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

