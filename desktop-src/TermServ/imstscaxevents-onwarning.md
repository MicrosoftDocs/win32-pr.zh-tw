---
title: IMsTscAxEvents OnWarning 方法
description: 當用戶端控制項遇到不嚴重的錯誤狀況時呼叫。
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- OnWarning 方法遠端桌面服務
- OnWarning 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnWarning 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686053"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="51e7f-106">IMsTscAxEvents：： OnWarning 方法</span><span class="sxs-lookup"><span data-stu-id="51e7f-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="51e7f-107">當用戶端控制項遇到不嚴重的錯誤狀況時呼叫。</span><span class="sxs-lookup"><span data-stu-id="51e7f-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e7f-108">語法</span><span class="sxs-lookup"><span data-stu-id="51e7f-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="51e7f-109">參數</span><span class="sxs-lookup"><span data-stu-id="51e7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e7f-110">*warningCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51e7f-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e7f-111">錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="51e7f-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="51e7f-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="51e7f-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="51e7f-113">點陣圖快取已損毀。</span><span class="sxs-lookup"><span data-stu-id="51e7f-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e7f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="51e7f-114">Return value</span></span>

<span data-ttu-id="51e7f-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="51e7f-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e7f-116">備註</span><span class="sxs-lookup"><span data-stu-id="51e7f-116">Remarks</span></span>

<span data-ttu-id="51e7f-117">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="51e7f-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51e7f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="51e7f-118">Requirements</span></span>



| <span data-ttu-id="51e7f-119">需求</span><span class="sxs-lookup"><span data-stu-id="51e7f-119">Requirement</span></span> | <span data-ttu-id="51e7f-120">值</span><span class="sxs-lookup"><span data-stu-id="51e7f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51e7f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51e7f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51e7f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51e7f-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="51e7f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51e7f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51e7f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51e7f-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="51e7f-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="51e7f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="51e7f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e7f-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="51e7f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="51e7f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51e7f-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e7f-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="51e7f-129">IID</span><span class="sxs-lookup"><span data-stu-id="51e7f-129">IID</span></span><br/>                      | <span data-ttu-id="51e7f-130">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="51e7f-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="51e7f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51e7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e7f-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="51e7f-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





