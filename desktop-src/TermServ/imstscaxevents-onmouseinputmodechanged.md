---
title: IMsTscAxEvents OnMouseInputModeChanged 方法
description: 當滑鼠輸入模式變更時呼叫。
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- OnMouseInputModeChanged 方法遠端桌面服務
- OnMouseInputModeChanged 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnMouseInputModeChanged 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104321"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="0b79c-106">IMsTscAxEvents：： OnMouseInputModeChanged 方法</span><span class="sxs-lookup"><span data-stu-id="0b79c-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="0b79c-107">當滑鼠輸入模式變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="0b79c-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b79c-108">語法</span><span class="sxs-lookup"><span data-stu-id="0b79c-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="0b79c-109">參數</span><span class="sxs-lookup"><span data-stu-id="0b79c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b79c-110">*fMouseModeRelative* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0b79c-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b79c-111">指出滑鼠是否處於相對模式。</span><span class="sxs-lookup"><span data-stu-id="0b79c-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b79c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b79c-112">Return value</span></span>

<span data-ttu-id="0b79c-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0b79c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b79c-114">備註</span><span class="sxs-lookup"><span data-stu-id="0b79c-114">Remarks</span></span>

<span data-ttu-id="0b79c-115">在事件接收中執行此方法，以接收滑鼠輸入模式已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="0b79c-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b79c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b79c-116">Requirements</span></span>



| <span data-ttu-id="0b79c-117">需求</span><span class="sxs-lookup"><span data-stu-id="0b79c-117">Requirement</span></span> | <span data-ttu-id="0b79c-118">值</span><span class="sxs-lookup"><span data-stu-id="0b79c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b79c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b79c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b79c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b79c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0b79c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b79c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b79c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b79c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0b79c-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0b79c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b79c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b79c-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b79c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0b79c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b79c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b79c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b79c-127">IID</span><span class="sxs-lookup"><span data-stu-id="0b79c-127">IID</span></span><br/>                      | <span data-ttu-id="0b79c-128">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0b79c-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0b79c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b79c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b79c-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="0b79c-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





