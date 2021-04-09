---
title: BasicDevice.remove_ConnectionStatusChanged 方法
description: 取消註冊 ConnectionStatusChanged 事件的事件處理常式。 |BasicDevice.remove_ConnectionStatusChanged 方法
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- remove_ConnectionStatusChanged 方法媒體串流 API
- remove_ConnectionStatusChanged 方法媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，remove_ConnectionStatusChanged 方法
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196044"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="f03eb-107">BasicDevice。移除 \_ ConnectionStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="f03eb-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="f03eb-108">取消註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f03eb-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03eb-109">語法</span><span class="sxs-lookup"><span data-stu-id="f03eb-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="f03eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="f03eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03eb-111">*token* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f03eb-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03eb-112">註冊事件處理常式時，從 [**add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) 方法取得的標記參考。</span><span class="sxs-lookup"><span data-stu-id="f03eb-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f03eb-113">Return value</span></span>

<span data-ttu-id="f03eb-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f03eb-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f03eb-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f03eb-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f03eb-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f03eb-116">Return code</span></span>                                                                          | <span data-ttu-id="f03eb-117">Description</span><span class="sxs-lookup"><span data-stu-id="f03eb-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f03eb-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f03eb-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f03eb-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f03eb-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f03eb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f03eb-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="f03eb-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f03eb-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

