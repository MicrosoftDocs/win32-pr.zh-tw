---
title: 'INapComponentConfig3 SetConfigToID 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來設定特定設定識別碼的設定資料。
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- SetConfigToID 方法 NAP
- SetConfigToID 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，SetConfigToID 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970015"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="99863-106">INapComponentConfig3：： SetConfigToID 方法</span><span class="sxs-lookup"><span data-stu-id="99863-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="99863-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="99863-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="99863-108">**SetConfigToID** 方法是由系統健康狀態驗證 (shv) 來提供一種方法，以設定特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="99863-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="99863-109">語法</span><span class="sxs-lookup"><span data-stu-id="99863-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="99863-110">參數</span><span class="sxs-lookup"><span data-stu-id="99863-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99863-111">*configID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99863-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99863-112">表示設定的值。</span><span class="sxs-lookup"><span data-stu-id="99863-112">A value that represents the configuration.</span></span> <span data-ttu-id="99863-113">網路原則伺服器 (NPS) 服務指派 *ConfigID* ，且在 SHV 內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="99863-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="99863-114">如果 *ConfigID* 為0，則會設定 SHV 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="99863-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="99863-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99863-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99863-116">*資料* 中設定資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="99863-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="99863-117">*資料* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99863-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99863-118">在輸入上，包含設定為 *ConfigID* 之設定資料的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="99863-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99863-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="99863-119">Return value</span></span>

<span data-ttu-id="99863-120">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99863-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="99863-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="99863-121">Return code</span></span>                                                                                                    | <span data-ttu-id="99863-122">Description</span><span class="sxs-lookup"><span data-stu-id="99863-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="99863-123"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="99863-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="99863-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="99863-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="99863-125"><dt>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="99863-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="99863-126">找不到 *ConfigID* 。</span><span class="sxs-lookup"><span data-stu-id="99863-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="99863-127">備註</span><span class="sxs-lookup"><span data-stu-id="99863-127">Remarks</span></span>

<span data-ttu-id="99863-128">在呼叫這個方法之前，必須先使用 [**>newconfig.json**](inapcomponentconfig3-newconfig.md) 方法來配置 *ConfigID* 的設定資料。</span><span class="sxs-lookup"><span data-stu-id="99863-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="99863-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="99863-129">Requirements</span></span>



| <span data-ttu-id="99863-130">需求</span><span class="sxs-lookup"><span data-stu-id="99863-130">Requirement</span></span> | <span data-ttu-id="99863-131">值</span><span class="sxs-lookup"><span data-stu-id="99863-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99863-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99863-132">Minimum supported client</span></span><br/> | <span data-ttu-id="99863-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="99863-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="99863-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99863-134">Minimum supported server</span></span><br/> | <span data-ttu-id="99863-135">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99863-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99863-136">標頭</span><span class="sxs-lookup"><span data-stu-id="99863-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="99863-137"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="99863-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="99863-138">Idl</span><span class="sxs-lookup"><span data-stu-id="99863-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99863-139"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="99863-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99863-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99863-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99863-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="99863-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





