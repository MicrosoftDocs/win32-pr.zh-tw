---
title: IMsRdpClient8 Reconnect 方法
description: 重新連接到具有新桌面寬度和高度的遠端會話。
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Reconnect 方法遠端桌面服務
- Reconnect 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務、Reconnect 方法
- Reconnect 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務、Reconnect 方法
- Reconnect 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務、Reconnect 方法
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509474"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="dc134-110">IMsRdpClient8：： Reconnect 方法</span><span class="sxs-lookup"><span data-stu-id="dc134-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="dc134-111">重新連接到具有新桌面寬度和高度的遠端會話。</span><span class="sxs-lookup"><span data-stu-id="dc134-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="dc134-112">控制項必須已連接到遠端會話，這個方法才能成功。</span><span class="sxs-lookup"><span data-stu-id="dc134-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc134-113">語法</span><span class="sxs-lookup"><span data-stu-id="dc134-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="dc134-114">參數</span><span class="sxs-lookup"><span data-stu-id="dc134-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc134-115">*ulWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc134-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc134-116">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="dc134-116">Type: **ULONG**</span></span>

<span data-ttu-id="dc134-117">新的桌面寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc134-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="dc134-118">如需值限制，請參閱 [**DesktopWidth**](imstscax-desktopwidth.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc134-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="dc134-119">*ulHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc134-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc134-120">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="dc134-120">Type: **ULONG**</span></span>

<span data-ttu-id="dc134-121">新的桌面高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc134-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="dc134-122">如需值限制，請參閱 [**DesktopHeight**](imstscax-desktopheight.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc134-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="dc134-123">*pReconnectStatus* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="dc134-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dc134-124">類型： \**[**ControlReconnectStatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="dc134-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="dc134-125">[_ *ControlReconnectStatus* \*](controlreconnectstatus.md)變數的指標，此變數會接收重新連接作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc134-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc134-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc134-126">Return value</span></span>

<span data-ttu-id="dc134-127">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc134-127">Type: **HRESULT**</span></span>

<span data-ttu-id="dc134-128">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dc134-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc134-129">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc134-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc134-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc134-130">Requirements</span></span>



| <span data-ttu-id="dc134-131">需求</span><span class="sxs-lookup"><span data-stu-id="dc134-131">Requirement</span></span> | <span data-ttu-id="dc134-132">值</span><span class="sxs-lookup"><span data-stu-id="dc134-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc134-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc134-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dc134-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dc134-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="dc134-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc134-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dc134-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc134-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="dc134-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dc134-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc134-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc134-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc134-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dc134-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc134-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc134-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc134-141">IID</span><span class="sxs-lookup"><span data-stu-id="dc134-141">IID</span></span><br/>                      | <span data-ttu-id="dc134-142">IID \_ IMsRdpClient8 定義為4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="dc134-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dc134-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc134-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc134-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="dc134-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="dc134-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="dc134-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="dc134-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="dc134-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="dc134-147">**ControlReconnectStatus**</span><span class="sxs-lookup"><span data-stu-id="dc134-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





