---
title: IBasicDevice remove_ConnectionStatusChanged 方法
description: 取消註冊 ConnectionStatusChanged 事件的事件處理常式。 |IBasicDevice remove_ConnectionStatusChanged 方法
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- remove_ConnectionStatusChanged 方法媒體串流 API
- remove_ConnectionStatusChanged 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，remove_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997349"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="d9921-107">IBasicDevice：： remove \_ ConnectionStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="d9921-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="d9921-108">取消註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="d9921-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9921-109">語法</span><span class="sxs-lookup"><span data-stu-id="d9921-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="d9921-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9921-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9921-111">*token* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9921-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9921-112">註冊事件處理常式時，從 [**add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) 方法取得的標記參考。</span><span class="sxs-lookup"><span data-stu-id="d9921-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9921-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9921-113">Return value</span></span>

<span data-ttu-id="d9921-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d9921-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d9921-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d9921-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d9921-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d9921-116">Return code</span></span>                                                                          | <span data-ttu-id="d9921-117">Description</span><span class="sxs-lookup"><span data-stu-id="d9921-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d9921-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d9921-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d9921-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d9921-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d9921-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9921-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9921-121">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="d9921-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





