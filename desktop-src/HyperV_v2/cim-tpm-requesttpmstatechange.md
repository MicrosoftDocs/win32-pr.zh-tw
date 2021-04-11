---
description: 要求將 TPM 的狀態變更為 RequestedTPMState 參數中指定的值。
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: CIM_TPM 類別的 RequestTPMStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943902"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="a0651-103">CIM TPM 類別的 RequestTPMStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a0651-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="a0651-104">要求將 TPM 的狀態變更為 *RequestedTPMState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="a0651-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="a0651-105">如果方法調用成功完成， **TPMState** 屬性應該等於 **RequestedTPMState** 參數。</span><span class="sxs-lookup"><span data-stu-id="a0651-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="a0651-106">多次叫用 **RequestTPMStateChange** 方法可能會導致較早的要求被覆寫或遺失。</span><span class="sxs-lookup"><span data-stu-id="a0651-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0651-107">語法</span><span class="sxs-lookup"><span data-stu-id="a0651-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a0651-108">參數</span><span class="sxs-lookup"><span data-stu-id="a0651-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0651-109">*RequestedTPMState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0651-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0651-110">要求的 TPM 狀態。</span><span class="sxs-lookup"><span data-stu-id="a0651-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="a0651-111">**已啟用 S1-Active-擁有的** (2) </span><span class="sxs-lookup"><span data-stu-id="a0651-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="a0651-112">**S2 已停用-Active-擁有的** (3) </span><span class="sxs-lookup"><span data-stu-id="a0651-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="a0651-113">**已啟用 S3-非使用中-擁有的** (4) </span><span class="sxs-lookup"><span data-stu-id="a0651-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="a0651-114">**已停用 S4-非使用中-擁有的** (5) </span><span class="sxs-lookup"><span data-stu-id="a0651-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="a0651-115">**已啟用 S5-主動-** 無人擁有的 (6) </span><span class="sxs-lookup"><span data-stu-id="a0651-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="a0651-116">**S6 已停用-主動-** 無人 (7) </span><span class="sxs-lookup"><span data-stu-id="a0651-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="a0651-117">**S7 已啟用-非** 使用中-無人擁有的 (8) </span><span class="sxs-lookup"><span data-stu-id="a0651-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="a0651-118">**S8 已停用-非** 使用中-無人擁有的 (9) </span><span class="sxs-lookup"><span data-stu-id="a0651-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a0651-119">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a0651-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a0651-120">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a0651-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a0651-121">*AuthorizationToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0651-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0651-122">可能需要的授權權杖，動作才會生效。</span><span class="sxs-lookup"><span data-stu-id="a0651-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="a0651-123">可能需要 *AuthorizationToken* 參數，才能建立實體存在，或傳遞 OWNERAUTH （TCG 定義的擁有者授權密碼）。</span><span class="sxs-lookup"><span data-stu-id="a0651-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="a0651-124">在 OwnerAuth 的案例中， \_ 可能需要 cim SharedCredential （具有非 null 值的 cim \_ SharedCredential）。</span><span class="sxs-lookup"><span data-stu-id="a0651-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="a0651-125">CIM \_ SharedCredential 演算法屬性也可以根據屬性 cim \_ TPMCapabilities. SupportedPasswordAlgorithms 來指定。</span><span class="sxs-lookup"><span data-stu-id="a0651-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="a0651-126">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a0651-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0651-127">可能包含建立之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 的參考，以追蹤方法調用所起始的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="a0651-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="a0651-128">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0651-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0651-129">指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。</span><span class="sxs-lookup"><span data-stu-id="a0651-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="a0651-130">間隔格式必須用來指定 *TimeoutPeriod*。</span><span class="sxs-lookup"><span data-stu-id="a0651-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="a0651-131">值為0或 null 參數表示用戶端沒有轉換的時間需求。</span><span class="sxs-lookup"><span data-stu-id="a0651-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0651-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0651-132">Return value</span></span>

<span data-ttu-id="a0651-133">成功時，會傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0651-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a0651-134">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a0651-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-135">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a0651-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-136">**未知或未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="a0651-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-137">**無法在 Timeout 期間內完成** (3) </span><span class="sxs-lookup"><span data-stu-id="a0651-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-138">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="a0651-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-139">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="a0651-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-140">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="a0651-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-141">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a0651-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-142">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a0651-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-143">**不正確狀態轉換** (4097) </span><span class="sxs-lookup"><span data-stu-id="a0651-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-144"> (4098) **不支援使用 Timeout 參數**</span><span class="sxs-lookup"><span data-stu-id="a0651-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-145">**忙碌** (4099) </span><span class="sxs-lookup"><span data-stu-id="a0651-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-146">**方法保留** (4100. 32767) </span><span class="sxs-lookup"><span data-stu-id="a0651-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a0651-147">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a0651-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a0651-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0651-148">Requirements</span></span>



| <span data-ttu-id="a0651-149">需求</span><span class="sxs-lookup"><span data-stu-id="a0651-149">Requirement</span></span> | <span data-ttu-id="a0651-150">值</span><span class="sxs-lookup"><span data-stu-id="a0651-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0651-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0651-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a0651-152">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0651-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a0651-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0651-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a0651-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a0651-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a0651-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0651-155">Namespace</span></span><br/>                | <span data-ttu-id="a0651-156">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a0651-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a0651-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a0651-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0651-158"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a0651-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0651-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a0651-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0651-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0651-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0651-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0651-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0651-162">**CIM \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="a0651-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




