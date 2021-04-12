---
title: IMsRdpClient9 attachEvent 方法
description: 附加事件。
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- attachEvent 方法遠端桌面服務
- attachEvent 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，attachEvent 方法
- attachEvent 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，attachEvent 方法
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464325"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="5ecae-108">IMsRdpClient9：： attachEvent 方法</span><span class="sxs-lookup"><span data-stu-id="5ecae-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="5ecae-109">附加事件。</span><span class="sxs-lookup"><span data-stu-id="5ecae-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ecae-110">語法</span><span class="sxs-lookup"><span data-stu-id="5ecae-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="5ecae-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ecae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ecae-112">*事件名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ecae-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecae-113">要附加的事件。</span><span class="sxs-lookup"><span data-stu-id="5ecae-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="5ecae-114">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ecae-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ecae-115">回呼。</span><span class="sxs-lookup"><span data-stu-id="5ecae-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ecae-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ecae-116">Return value</span></span>

<span data-ttu-id="5ecae-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5ecae-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ecae-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5ecae-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecae-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ecae-119">Requirements</span></span>



| <span data-ttu-id="5ecae-120">需求</span><span class="sxs-lookup"><span data-stu-id="5ecae-120">Requirement</span></span> | <span data-ttu-id="5ecae-121">值</span><span class="sxs-lookup"><span data-stu-id="5ecae-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecae-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ecae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecae-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5ecae-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5ecae-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ecae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecae-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5ecae-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="5ecae-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5ecae-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ecae-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecae-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="5ecae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5ecae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ecae-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ecae-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="5ecae-130">IID</span><span class="sxs-lookup"><span data-stu-id="5ecae-130">IID</span></span><br/>                      | <span data-ttu-id="5ecae-131">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="5ecae-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="5ecae-132">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="5ecae-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="5ecae-133">IID \_ IMsRdpClient9 定義為28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="5ecae-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ecae-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ecae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecae-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="5ecae-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="5ecae-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5ecae-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





