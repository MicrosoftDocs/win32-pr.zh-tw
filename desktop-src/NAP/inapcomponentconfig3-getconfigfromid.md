---
title: 'INapComponentConfig3 GetConfigFromID 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來取得特定設定識別碼的設定資料。
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- GetConfigFromID 方法 NAP
- GetConfigFromID 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，GetConfigFromID 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685767"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="61239-106">INapComponentConfig3：： GetConfigFromID 方法</span><span class="sxs-lookup"><span data-stu-id="61239-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="61239-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="61239-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="61239-108">**GetConfigFromID** 方法是由系統健康狀態驗證 (shv) 來提供方法，以取得特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="61239-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="61239-109">語法</span><span class="sxs-lookup"><span data-stu-id="61239-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="61239-110">參數</span><span class="sxs-lookup"><span data-stu-id="61239-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61239-111">*configID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61239-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61239-112">表示設定的值。</span><span class="sxs-lookup"><span data-stu-id="61239-112">A value that represents the configuration.</span></span> <span data-ttu-id="61239-113">如果 *ConfigID* 為 **0**，SHV 應該會傳回 *outdata* 中的預設設定資料。</span><span class="sxs-lookup"><span data-stu-id="61239-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="61239-114">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61239-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61239-115">*Outdata* 中傳回的設定資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="61239-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="61239-116">*outdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61239-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61239-117">傳回時，包含 *ConfigID* 所代表之設定資料的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="61239-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61239-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="61239-118">Return value</span></span>

<span data-ttu-id="61239-119">根據此操作的結果，傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61239-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="61239-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="61239-120">Return code</span></span>                                                                                                    | <span data-ttu-id="61239-121">Description</span><span class="sxs-lookup"><span data-stu-id="61239-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="61239-122"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="61239-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="61239-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="61239-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="61239-124"><dt>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="61239-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="61239-125">找不到 *ConfigID* 。</span><span class="sxs-lookup"><span data-stu-id="61239-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="61239-126">備註</span><span class="sxs-lookup"><span data-stu-id="61239-126">Remarks</span></span>

<span data-ttu-id="61239-127">在呼叫這個方法之前，必須先使用 [**>newconfig.json**](inapcomponentconfig3-newconfig.md) 方法來配置 *ConfigID* 的設定資料。</span><span class="sxs-lookup"><span data-stu-id="61239-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="61239-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="61239-128">Requirements</span></span>



| <span data-ttu-id="61239-129">需求</span><span class="sxs-lookup"><span data-stu-id="61239-129">Requirement</span></span> | <span data-ttu-id="61239-130">值</span><span class="sxs-lookup"><span data-stu-id="61239-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61239-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61239-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61239-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="61239-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="61239-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61239-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61239-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61239-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61239-135">標頭</span><span class="sxs-lookup"><span data-stu-id="61239-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="61239-136"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="61239-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="61239-137">Idl</span><span class="sxs-lookup"><span data-stu-id="61239-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61239-138"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="61239-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61239-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61239-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61239-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="61239-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





