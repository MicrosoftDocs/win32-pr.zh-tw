---
title: IMsRdpClient9 Vemap.detachevent 方法
description: 卸離事件。
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Vemap.detachevent 方法遠端桌面服務
- Vemap.detachevent 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，Vemap.detachevent 方法
- Vemap.detachevent 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，Vemap.detachevent 方法
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093888"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="df86e-108">IMsRdpClient9：:d etachEvent 方法</span><span class="sxs-lookup"><span data-stu-id="df86e-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="df86e-109">卸離事件。</span><span class="sxs-lookup"><span data-stu-id="df86e-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="df86e-110">語法</span><span class="sxs-lookup"><span data-stu-id="df86e-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="df86e-111">參數</span><span class="sxs-lookup"><span data-stu-id="df86e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df86e-112">*事件名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df86e-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df86e-113">活動的名稱。</span><span class="sxs-lookup"><span data-stu-id="df86e-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="df86e-114">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df86e-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df86e-115">與事件相關聯的回呼。</span><span class="sxs-lookup"><span data-stu-id="df86e-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df86e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="df86e-116">Return value</span></span>

<span data-ttu-id="df86e-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="df86e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df86e-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="df86e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df86e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="df86e-119">Requirements</span></span>



| <span data-ttu-id="df86e-120">需求</span><span class="sxs-lookup"><span data-stu-id="df86e-120">Requirement</span></span> | <span data-ttu-id="df86e-121">值</span><span class="sxs-lookup"><span data-stu-id="df86e-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df86e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df86e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df86e-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df86e-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="df86e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df86e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df86e-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df86e-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="df86e-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df86e-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="df86e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df86e-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="df86e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="df86e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df86e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df86e-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="df86e-130">IID</span><span class="sxs-lookup"><span data-stu-id="df86e-130">IID</span></span><br/>                      | <span data-ttu-id="df86e-131">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="df86e-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="df86e-132">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="df86e-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="df86e-133">IID \_ IMsRdpClient9 定義為28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="df86e-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df86e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df86e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df86e-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="df86e-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="df86e-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="df86e-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





