---
title: 'INapComponentConfig InvokeUI 方法 (NapCommon .h) '
description: 針對 (SHV) 元件的系統健全狀況驗證程式啟動自訂使用者介面。
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- InvokeUI 方法 NAP
- InvokeUI 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，InvokeUI 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934172"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="000ed-106">INapComponentConfig：： InvokeUI 方法</span><span class="sxs-lookup"><span data-stu-id="000ed-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="000ed-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="000ed-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="000ed-108">**InvokeUI** 方法會針對 (SHV) 元件的系統健全狀況驗證程式啟動自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="000ed-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="000ed-109">語法</span><span class="sxs-lookup"><span data-stu-id="000ed-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="000ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="000ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000ed-111">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="000ed-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="000ed-112">父系或擁有者視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="000ed-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="000ed-113">必須提供有效的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="000ed-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000ed-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="000ed-114">Return value</span></span>

<span data-ttu-id="000ed-115">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="000ed-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="000ed-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="000ed-116">Return code</span></span>                                                                                     | <span data-ttu-id="000ed-117">Description</span><span class="sxs-lookup"><span data-stu-id="000ed-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="000ed-118"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="000ed-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="000ed-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="000ed-120"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="000ed-121">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="000ed-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="000ed-122"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="000ed-123">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="000ed-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="000ed-124"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="000ed-125">SHV 不支援自訂的 UI。</span><span class="sxs-lookup"><span data-stu-id="000ed-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="000ed-126">備註</span><span class="sxs-lookup"><span data-stu-id="000ed-126">Remarks</span></span>

<span data-ttu-id="000ed-127">此方法呼叫應該會封鎖，直到 SHV 使用者介面結束為止。</span><span class="sxs-lookup"><span data-stu-id="000ed-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="000ed-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="000ed-128">Requirements</span></span>



| <span data-ttu-id="000ed-129">需求</span><span class="sxs-lookup"><span data-stu-id="000ed-129">Requirement</span></span> | <span data-ttu-id="000ed-130">值</span><span class="sxs-lookup"><span data-stu-id="000ed-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="000ed-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="000ed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="000ed-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="000ed-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="000ed-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="000ed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="000ed-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="000ed-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="000ed-135">標頭</span><span class="sxs-lookup"><span data-stu-id="000ed-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="000ed-136"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="000ed-137">Idl</span><span class="sxs-lookup"><span data-stu-id="000ed-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="000ed-138"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="000ed-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000ed-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="000ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000ed-140">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="000ed-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="000ed-141">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="000ed-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





