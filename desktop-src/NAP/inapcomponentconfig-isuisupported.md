---
title: 'INapComponentConfig IsUISupported 方法 (NapCommon .h) '
description: 指定元件是否支援自訂的使用者介面。
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- IsUISupported 方法 NAP
- IsUISupported 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，IsUISupported 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965299"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="38098-106">INapComponentConfig：： IsUISupported 方法</span><span class="sxs-lookup"><span data-stu-id="38098-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="38098-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="38098-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="38098-108">**IsUISupported** 方法會指定元件是否支援自訂的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="38098-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="38098-109">語法</span><span class="sxs-lookup"><span data-stu-id="38098-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="38098-110">參數</span><span class="sxs-lookup"><span data-stu-id="38098-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38098-111">*isSupported* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="38098-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38098-112">如果元件支援自訂的使用者介面，則為布林 **值** 的指標，如果是，則為 FALSE，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="38098-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38098-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="38098-113">Return value</span></span>

<span data-ttu-id="38098-114">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="38098-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="38098-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="38098-115">Return code</span></span>                                                                                     | <span data-ttu-id="38098-116">Description</span><span class="sxs-lookup"><span data-stu-id="38098-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="38098-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="38098-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="38098-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="38098-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="38098-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="38098-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="38098-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="38098-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="38098-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="38098-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="38098-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="38098-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38098-123">備註</span><span class="sxs-lookup"><span data-stu-id="38098-123">Remarks</span></span>

<span data-ttu-id="38098-124">應該使用 [**INapComponentConfig：： InvokeUI**](inapcomponentconfig-invokeui.md)來啟動元件的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="38098-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38098-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="38098-125">Requirements</span></span>



| <span data-ttu-id="38098-126">需求</span><span class="sxs-lookup"><span data-stu-id="38098-126">Requirement</span></span> | <span data-ttu-id="38098-127">值</span><span class="sxs-lookup"><span data-stu-id="38098-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38098-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38098-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38098-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="38098-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="38098-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38098-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38098-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38098-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="38098-132">標頭</span><span class="sxs-lookup"><span data-stu-id="38098-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="38098-133"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="38098-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="38098-134">Idl</span><span class="sxs-lookup"><span data-stu-id="38098-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38098-135"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="38098-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38098-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38098-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38098-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="38098-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="38098-138">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="38098-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





