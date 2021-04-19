---
title: IBasicDevice add_ConnectionStatusChanged 方法
description: 註冊 ConnectionStatusChanged 事件的事件處理常式。 |IBasicDevice add_ConnectionStatusChanged 方法
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- add_ConnectionStatusChanged 方法媒體串流 API
- add_ConnectionStatusChanged 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，add_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992687"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="4ffac-107">IBasicDevice：： add \_ ConnectionStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="4ffac-107">IBasicDevice::add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="4ffac-108">註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4ffac-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffac-109">語法</span><span class="sxs-lookup"><span data-stu-id="4ffac-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="4ffac-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ffac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ffac-111">*處理常式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ffac-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-112">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))事件處理常式函數。</span><span class="sxs-lookup"><span data-stu-id="4ffac-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="4ffac-113">*token* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4ffac-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-114">可以用來取消註冊事件處理常式之權杖的參考。</span><span class="sxs-lookup"><span data-stu-id="4ffac-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ffac-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ffac-115">Return value</span></span>

<span data-ttu-id="4ffac-116">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4ffac-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4ffac-117">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4ffac-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4ffac-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4ffac-118">Return code</span></span>                                                                          | <span data-ttu-id="4ffac-119">Description</span><span class="sxs-lookup"><span data-stu-id="4ffac-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4ffac-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4ffac-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4ffac-121">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4ffac-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ffac-122">備註</span><span class="sxs-lookup"><span data-stu-id="4ffac-122">Remarks</span></span>

<span data-ttu-id="4ffac-123">若要取消註冊這個方法所註冊的事件處理常式，請將 *權杖* 值傳遞給 [**remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4ffac-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ffac-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ffac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ffac-125">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4ffac-125">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

