---
title: 'INapSoHConstructor AppendAttribute 方法 (NapProtocol .h) '
description: 將 TLV 新增至 SoH 緩衝區的結尾。
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- AppendAttribute 方法 NAP
- AppendAttribute 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，AppendAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508528"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="48c33-106">INapSoHConstructor：： AppendAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="48c33-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="48c33-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="48c33-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="48c33-108">**INapSoHConstructor：： AppendAttribute** 方法會將 TLV 新增至 SoH 緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="48c33-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c33-109">語法</span><span class="sxs-lookup"><span data-stu-id="48c33-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="48c33-110">參數</span><span class="sxs-lookup"><span data-stu-id="48c33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c33-111">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c33-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c33-112">[**SoHAttributeType**](sohattributetype-enum.md)列舉，指出新的 TLV 的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="48c33-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="48c33-113">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c33-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c33-114">[**SoHAttributeValue**](sohattributevalue-union.md)結構的指標，其中包含新的 TLV 的值。</span><span class="sxs-lookup"><span data-stu-id="48c33-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c33-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="48c33-115">Return value</span></span>

<span data-ttu-id="48c33-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="48c33-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="48c33-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="48c33-117">Return code</span></span>                                                                                     | <span data-ttu-id="48c33-118">Description</span><span class="sxs-lookup"><span data-stu-id="48c33-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="48c33-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="48c33-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="48c33-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="48c33-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="48c33-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="48c33-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="48c33-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="48c33-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="48c33-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48c33-125">備註</span><span class="sxs-lookup"><span data-stu-id="48c33-125">Remarks</span></span>

<span data-ttu-id="48c33-126">不能使用此函式來新增 [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="48c33-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="48c33-127">它會新增為 [**INapSoHConstructor：： Initialize**](inapsohconstructor-initialize-method.md) 到新建立之 SOH 封包的第一個 TLV。</span><span class="sxs-lookup"><span data-stu-id="48c33-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="48c33-128">附加 Nap 系統將使用的屬性時，不應以任何方式加密或修改。</span><span class="sxs-lookup"><span data-stu-id="48c33-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="48c33-129">如果 HealthEntity 需要加密/完整性檢查 (Mac) 私用資訊，它只應包含在 [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="48c33-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c33-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="48c33-130">Requirements</span></span>



| <span data-ttu-id="48c33-131">需求</span><span class="sxs-lookup"><span data-stu-id="48c33-131">Requirement</span></span> | <span data-ttu-id="48c33-132">值</span><span class="sxs-lookup"><span data-stu-id="48c33-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c33-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48c33-133">Minimum supported client</span></span><br/> | <span data-ttu-id="48c33-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48c33-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48c33-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48c33-135">Minimum supported server</span></span><br/> | <span data-ttu-id="48c33-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48c33-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="48c33-137">標頭</span><span class="sxs-lookup"><span data-stu-id="48c33-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="48c33-138"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="48c33-139">Idl</span><span class="sxs-lookup"><span data-stu-id="48c33-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48c33-140"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="48c33-141">DLL</span><span class="sxs-lookup"><span data-stu-id="48c33-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c33-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c33-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="48c33-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48c33-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c33-144">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="48c33-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





