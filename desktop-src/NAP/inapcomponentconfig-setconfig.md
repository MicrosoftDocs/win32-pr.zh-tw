---
title: 'INapComponentConfig SetConfig 方法 (NapCommon .h) '
description: 設定 (SHV) 元件設定的系統健全狀況驗證程式。
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- SetConfig 方法 NAP
- SetConfig 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，SetConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509483"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="b6127-106">INapComponentConfig：： SetConfig 方法</span><span class="sxs-lookup"><span data-stu-id="b6127-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="b6127-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b6127-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b6127-108">**SetConfig** 方法會設定 (SHV) 元件設定的系統健全狀況驗證程式。</span><span class="sxs-lookup"><span data-stu-id="b6127-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6127-109">語法</span><span class="sxs-lookup"><span data-stu-id="b6127-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="b6127-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6127-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6127-111">*bCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6127-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6127-112">*資料* 設定 blob 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6127-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="b6127-113">*資料* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6127-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6127-114">SHV 元件設定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="b6127-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="b6127-115">使用 [**GetConfig**](inapcomponentconfig-getconfig.md) 方法從 x86 電腦匯出的設定資料，可以使用 **SetConfig** 方法匯入至 x64 電腦，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b6127-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="b6127-116">因此，設定資料的格式必須是與架構無關的格式，例如 XML。</span><span class="sxs-lookup"><span data-stu-id="b6127-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="b6127-117">使用 XML 而非位元組資料流程可讓您更輕鬆地在不同的架構上使用設定資料。</span><span class="sxs-lookup"><span data-stu-id="b6127-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="b6127-118">設定資料中使用的 XML 元素是由實施者決定。</span><span class="sxs-lookup"><span data-stu-id="b6127-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6127-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6127-119">Return value</span></span>

<span data-ttu-id="b6127-120">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b6127-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="b6127-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6127-121">Return code</span></span>                                                                                     | <span data-ttu-id="b6127-122">Description</span><span class="sxs-lookup"><span data-stu-id="b6127-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6127-123"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b6127-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b6127-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b6127-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b6127-125"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b6127-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b6127-126">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="b6127-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b6127-127"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6127-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b6127-128">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b6127-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6127-129">備註</span><span class="sxs-lookup"><span data-stu-id="b6127-129">Remarks</span></span>

<span data-ttu-id="b6127-130">元件版本設定資訊應包含在 *資料* 設定 blob 中。</span><span class="sxs-lookup"><span data-stu-id="b6127-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="b6127-131">從一個 SHV 版本遷移到另一個版本時，可能會使用版本設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b6127-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6127-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6127-132">Requirements</span></span>



| <span data-ttu-id="b6127-133">需求</span><span class="sxs-lookup"><span data-stu-id="b6127-133">Requirement</span></span> | <span data-ttu-id="b6127-134">值</span><span class="sxs-lookup"><span data-stu-id="b6127-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6127-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6127-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b6127-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="b6127-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b6127-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6127-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b6127-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6127-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b6127-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b6127-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6127-140"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6127-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6127-141">Idl</span><span class="sxs-lookup"><span data-stu-id="b6127-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6127-142"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6127-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6127-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6127-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6127-144">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="b6127-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="b6127-145">**INapConponentConfig::GetConfig**</span><span class="sxs-lookup"><span data-stu-id="b6127-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





