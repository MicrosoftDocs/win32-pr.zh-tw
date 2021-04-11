---
title: 'INapComponentConfig2 InvokeUIFromConfigBlob 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv) 視需要在記憶體中載入遠端或本機電腦的設定，並顯示允許操作設定資料的 UI。
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- InvokeUIFromConfigBlob 方法 NAP
- InvokeUIFromConfigBlob 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，InvokeUIFromConfigBlob 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843339"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="e19a1-106">INapComponentConfig2：： InvokeUIFromConfigBlob 方法</span><span class="sxs-lookup"><span data-stu-id="e19a1-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="e19a1-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="e19a1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e19a1-108">**InvokeUIFromConfigBlob** 方法是由系統健康狀態驗證 (shv) 視需要在記憶體中載入遠端或本機電腦的設定，並顯示允許操作設定資料的 UI。</span><span class="sxs-lookup"><span data-stu-id="e19a1-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="e19a1-109">Configuration 元件必須支援透過 DCOM 使用 [**INapComponentConfig**](inapcomponentconfig.md) 。</span><span class="sxs-lookup"><span data-stu-id="e19a1-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="e19a1-110">語法</span><span class="sxs-lookup"><span data-stu-id="e19a1-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="e19a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="e19a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19a1-112">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-113">父系或擁有者視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e19a1-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="e19a1-114">必須提供有效的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="e19a1-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="e19a1-115">*inbCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-116">*InData* 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e19a1-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="e19a1-117">*inData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-118">儲存初始設定資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e19a1-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="e19a1-119">這項資料會從遠端或本機電腦匯出。</span><span class="sxs-lookup"><span data-stu-id="e19a1-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="e19a1-120">*outbCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-121">*Outdata* 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e19a1-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="e19a1-122">*outdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-123">緩衝區的指標，此緩衝區會儲存由 SHV 設定使用者介面變更的設定資料。</span><span class="sxs-lookup"><span data-stu-id="e19a1-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="e19a1-124">這項資料是由遠端或本機電腦匯入。</span><span class="sxs-lookup"><span data-stu-id="e19a1-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="e19a1-125">*fConfigChanged* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e19a1-126">**布林** 值的指標，如果在 UI 作業期間變更設定，則設定為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e19a1-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19a1-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="e19a1-127">Return value</span></span>

<span data-ttu-id="e19a1-128">\_如果成功或其中一個標準 Windows 錯誤碼，則會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="e19a1-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e19a1-129">備註</span><span class="sxs-lookup"><span data-stu-id="e19a1-129">Remarks</span></span>

<span data-ttu-id="e19a1-130">如果用於本機電腦，則此函式可用於每個原則 SHV 設定。</span><span class="sxs-lookup"><span data-stu-id="e19a1-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="e19a1-131">它提供一種方法來叫用 SHV UI 和編輯現有的 SHV 設定。</span><span class="sxs-lookup"><span data-stu-id="e19a1-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19a1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e19a1-132">Requirements</span></span>



| <span data-ttu-id="e19a1-133">需求</span><span class="sxs-lookup"><span data-stu-id="e19a1-133">Requirement</span></span> | <span data-ttu-id="e19a1-134">值</span><span class="sxs-lookup"><span data-stu-id="e19a1-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e19a1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e19a1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e19a1-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="e19a1-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e19a1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e19a1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e19a1-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e19a1-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e19a1-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e19a1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19a1-140"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="e19a1-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e19a1-141">Idl</span><span class="sxs-lookup"><span data-stu-id="e19a1-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e19a1-142"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e19a1-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19a1-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e19a1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19a1-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="e19a1-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





