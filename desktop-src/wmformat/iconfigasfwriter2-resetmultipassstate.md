---
title: IConfigAsfWriter2 ResetMultiPassState 方法
description: 當前置處理編碼階段在完成之前取消時，ResetMultiPassState 方法會重設篩選。
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- ResetMultiPassState 方法 windows Media 格式
- ResetMultiPassState 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，ResetMultiPassState 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376292"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="16a8f-106">IConfigAsfWriter2：： ResetMultiPassState 方法</span><span class="sxs-lookup"><span data-stu-id="16a8f-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="16a8f-107">當前置處理編碼階段在完成之前取消時， **ResetMultiPassState** 方法會重設篩選。</span><span class="sxs-lookup"><span data-stu-id="16a8f-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a8f-108">語法</span><span class="sxs-lookup"><span data-stu-id="16a8f-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="16a8f-109">參數</span><span class="sxs-lookup"><span data-stu-id="16a8f-109">Parameters</span></span>

<span data-ttu-id="16a8f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="16a8f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16a8f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16a8f-111">Return value</span></span>

<span data-ttu-id="16a8f-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="16a8f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="16a8f-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="16a8f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="16a8f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="16a8f-114">Return code</span></span>                                                                                         | <span data-ttu-id="16a8f-115">Description</span><span class="sxs-lookup"><span data-stu-id="16a8f-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="16a8f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="16a8f-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="16a8f-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="16a8f-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="16a8f-118"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="16a8f-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="16a8f-119">篩選未處於已停止狀態。</span><span class="sxs-lookup"><span data-stu-id="16a8f-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16a8f-120">備註</span><span class="sxs-lookup"><span data-stu-id="16a8f-120">Remarks</span></span>

<span data-ttu-id="16a8f-121">只要在篩選器收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理編碼階段，就必須呼叫這個方法來重設篩選的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="16a8f-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="16a8f-122">如果前置處理編碼傳遞完成而沒有錯誤，則不需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="16a8f-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="16a8f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16a8f-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="16a8f-124">[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16a8f-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

