---
title: 'INapComponentConfig GetConfig 方法 (NapCommon .h) '
description: 抓取 (SHV) 元件設定的系統健全狀況驗證程式。
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig 方法 NAP
- GetConfig 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，GetConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466460"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="e13be-106">INapComponentConfig：： GetConfig 方法</span><span class="sxs-lookup"><span data-stu-id="e13be-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="e13be-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="e13be-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e13be-108">**GetConfig** 方法會 (SHV) 元件設定來抓取系統健全狀況驗證程式。</span><span class="sxs-lookup"><span data-stu-id="e13be-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13be-109">語法</span><span class="sxs-lookup"><span data-stu-id="e13be-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="e13be-110">參數</span><span class="sxs-lookup"><span data-stu-id="e13be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13be-111">*bCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e13be-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13be-112">*資料* 設定 blob 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e13be-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="e13be-113">*資料* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e13be-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13be-114">SHV 元件設定資料的位址指標。</span><span class="sxs-lookup"><span data-stu-id="e13be-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="e13be-115">使用 **GetConfig** 方法從 x86 電腦匯出的設定資料，可以使用 [**SetConfig**](inapcomponentconfig-setconfig.md) 方法匯入至 x64 電腦，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="e13be-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="e13be-116">因此，設定資料的格式必須是與架構無關的格式，例如 XML。</span><span class="sxs-lookup"><span data-stu-id="e13be-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="e13be-117">使用 XML 而非位元組資料流程可讓您更輕鬆地在不同的架構上使用設定資料。</span><span class="sxs-lookup"><span data-stu-id="e13be-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="e13be-118">設定資料中使用的 XML 元素是由實施者決定。</span><span class="sxs-lookup"><span data-stu-id="e13be-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13be-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e13be-119">Return value</span></span>

<span data-ttu-id="e13be-120">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e13be-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e13be-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e13be-121">Return code</span></span>                                                                                     | <span data-ttu-id="e13be-122">Description</span><span class="sxs-lookup"><span data-stu-id="e13be-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e13be-123"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e13be-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e13be-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e13be-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e13be-125"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e13be-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e13be-126">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e13be-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e13be-127"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e13be-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e13be-128">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e13be-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e13be-129">備註</span><span class="sxs-lookup"><span data-stu-id="e13be-129">Remarks</span></span>

<span data-ttu-id="e13be-130">資料參數必須由被呼叫端配置 (元件實作項) 使用 **CoTaskMemAlloc** ，並由呼叫者使用 **CoTaskMemFree** 釋放。</span><span class="sxs-lookup"><span data-stu-id="e13be-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13be-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e13be-131">Requirements</span></span>



| <span data-ttu-id="e13be-132">需求</span><span class="sxs-lookup"><span data-stu-id="e13be-132">Requirement</span></span> | <span data-ttu-id="e13be-133">值</span><span class="sxs-lookup"><span data-stu-id="e13be-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13be-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e13be-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e13be-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="e13be-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e13be-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e13be-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e13be-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e13be-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e13be-138">標頭</span><span class="sxs-lookup"><span data-stu-id="e13be-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13be-139"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="e13be-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e13be-140">Idl</span><span class="sxs-lookup"><span data-stu-id="e13be-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e13be-141"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e13be-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13be-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e13be-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13be-143">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="e13be-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="e13be-144">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="e13be-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





