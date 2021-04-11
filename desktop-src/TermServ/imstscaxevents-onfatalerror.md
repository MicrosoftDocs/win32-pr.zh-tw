---
title: IMsTscAxEvents OnFatalError 方法
description: 當用戶端控制項遇到嚴重錯誤時呼叫。
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- OnFatalError 方法遠端桌面服務
- OnFatalError 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnFatalError 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843848"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="9fc57-106">IMsTscAxEvents：： OnFatalError 方法</span><span class="sxs-lookup"><span data-stu-id="9fc57-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="9fc57-107">當用戶端控制項遇到嚴重錯誤時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9fc57-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc57-108">語法</span><span class="sxs-lookup"><span data-stu-id="9fc57-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="9fc57-109">參數</span><span class="sxs-lookup"><span data-stu-id="9fc57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc57-110">*errorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fc57-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc57-111">指示錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9fc57-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9fc57-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="9fc57-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-113">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fc57-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9fc57-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9fc57-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-115">內部錯誤碼1。</span><span class="sxs-lookup"><span data-stu-id="9fc57-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="9fc57-116"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="9fc57-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-117">發生記憶體不足的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fc57-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="9fc57-118"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="9fc57-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-119">發生視窗建立錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fc57-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="9fc57-120"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="9fc57-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-121">內部錯誤代碼2。</span><span class="sxs-lookup"><span data-stu-id="9fc57-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="9fc57-122"><span id="5"></span>**.5**</span><span class="sxs-lookup"><span data-stu-id="9fc57-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-123">內部錯誤代碼3。</span><span class="sxs-lookup"><span data-stu-id="9fc57-123">Internal error code 3.</span></span> <span data-ttu-id="9fc57-124">這不是有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="9fc57-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="9fc57-125"><span id="6"></span>**6**</span><span class="sxs-lookup"><span data-stu-id="9fc57-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-126">內部錯誤代碼4。</span><span class="sxs-lookup"><span data-stu-id="9fc57-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="9fc57-127"><span id="7"></span>**型**</span><span class="sxs-lookup"><span data-stu-id="9fc57-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-128">用戶端連接時發生無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fc57-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="9fc57-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="9fc57-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="9fc57-130">Winsock 初始化錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fc57-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc57-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fc57-131">Return value</span></span>

<span data-ttu-id="9fc57-132">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9fc57-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc57-133">備註</span><span class="sxs-lookup"><span data-stu-id="9fc57-133">Remarks</span></span>

<span data-ttu-id="9fc57-134">為了回應此事件，容器會顯示錯誤訊息並關閉。</span><span class="sxs-lookup"><span data-stu-id="9fc57-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="9fc57-135">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="9fc57-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc57-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fc57-136">Requirements</span></span>



| <span data-ttu-id="9fc57-137">需求</span><span class="sxs-lookup"><span data-stu-id="9fc57-137">Requirement</span></span> | <span data-ttu-id="9fc57-138">值</span><span class="sxs-lookup"><span data-stu-id="9fc57-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc57-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fc57-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc57-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fc57-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9fc57-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fc57-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc57-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc57-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9fc57-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9fc57-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fc57-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc57-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fc57-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc57-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc57-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc57-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fc57-147">IID</span><span class="sxs-lookup"><span data-stu-id="9fc57-147">IID</span></span><br/>                      | <span data-ttu-id="9fc57-148">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9fc57-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9fc57-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fc57-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc57-150">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9fc57-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





