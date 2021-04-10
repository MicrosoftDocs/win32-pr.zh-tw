---
description: Win32 Tpm 類別的 IsActivated 方法 \_ 會指出裝置是否已啟用。
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Win32_Tpm 類別的 IsActivated 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194168"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="55c42-103">Win32 Tpm 類別的 IsActivated 方法 \_</span><span class="sxs-lookup"><span data-stu-id="55c42-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="55c42-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsActivated** 方法會指出裝置是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="55c42-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c42-105">語法</span><span class="sxs-lookup"><span data-stu-id="55c42-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="55c42-106">參數</span><span class="sxs-lookup"><span data-stu-id="55c42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c42-107">*IsActivated* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55c42-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55c42-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="55c42-108">Type: **boolean**</span></span>

<span data-ttu-id="55c42-109">若 **為 true**，則會啟用裝置。</span><span class="sxs-lookup"><span data-stu-id="55c42-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="55c42-110">Return value</span></span>

<span data-ttu-id="55c42-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="55c42-111">Type: **uint32**</span></span>

<span data-ttu-id="55c42-112">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="55c42-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="55c42-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="55c42-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="55c42-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="55c42-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="55c42-115">Description</span><span class="sxs-lookup"><span data-stu-id="55c42-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="55c42-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="55c42-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="55c42-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="55c42-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55c42-118">備註</span><span class="sxs-lookup"><span data-stu-id="55c42-118">Remarks</span></span>

<span data-ttu-id="55c42-119">停用類似于停用，但可能發生操作狀態變更。</span><span class="sxs-lookup"><span data-stu-id="55c42-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="55c42-120">根據受信任的運算群組 (TCG) 1.2 規格，只有在裝置處於停用狀態時，才能使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="55c42-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="55c42-121">TPM \_ ContinueSelfTest</span><span class="sxs-lookup"><span data-stu-id="55c42-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="55c42-122">TPM \_ DSAP</span><span class="sxs-lookup"><span data-stu-id="55c42-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="55c42-123">TPM \_ FlushSpecific</span><span class="sxs-lookup"><span data-stu-id="55c42-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="55c42-124">TPM \_ GetCapability</span><span class="sxs-lookup"><span data-stu-id="55c42-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="55c42-125">TPM \_ GetTestResult</span><span class="sxs-lookup"><span data-stu-id="55c42-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="55c42-126">TPM \_ 初始化</span><span class="sxs-lookup"><span data-stu-id="55c42-126">TPM\_Init</span></span>
-   <span data-ttu-id="55c42-127">TPM \_ OIAP</span><span class="sxs-lookup"><span data-stu-id="55c42-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="55c42-128">TPM \_ OSAP</span><span class="sxs-lookup"><span data-stu-id="55c42-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="55c42-129">TPM \_ OwnerSetDisable</span><span class="sxs-lookup"><span data-stu-id="55c42-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="55c42-130">TPM \_ PCR \_ 重設</span><span class="sxs-lookup"><span data-stu-id="55c42-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="55c42-131">TPM \_ PhysicalDisable</span><span class="sxs-lookup"><span data-stu-id="55c42-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="55c42-132">TPM \_ PhysicalEnable</span><span class="sxs-lookup"><span data-stu-id="55c42-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="55c42-133">TPM \_ PhysicalSetDeactivated</span><span class="sxs-lookup"><span data-stu-id="55c42-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="55c42-134">TPM \_ 重設</span><span class="sxs-lookup"><span data-stu-id="55c42-134">TPM\_Reset</span></span>
-   <span data-ttu-id="55c42-135">TPM \_ SaveState</span><span class="sxs-lookup"><span data-stu-id="55c42-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="55c42-136">TPM \_ SelfTestFull</span><span class="sxs-lookup"><span data-stu-id="55c42-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="55c42-137">TPM \_ SetCapability</span><span class="sxs-lookup"><span data-stu-id="55c42-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="55c42-138">TPM \_ SHA1Complete</span><span class="sxs-lookup"><span data-stu-id="55c42-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="55c42-139">TPM \_ SHA1Start</span><span class="sxs-lookup"><span data-stu-id="55c42-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="55c42-140">TPM \_ SHA1Update</span><span class="sxs-lookup"><span data-stu-id="55c42-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="55c42-141">TPM \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="55c42-141">TPM\_Startup</span></span>
-   <span data-ttu-id="55c42-142">TPM \_ TakeOwnership</span><span class="sxs-lookup"><span data-stu-id="55c42-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="55c42-143">TPM \_ 終止 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="55c42-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="55c42-144">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="55c42-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55c42-145">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="55c42-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="55c42-146">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="55c42-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55c42-147">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="55c42-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55c42-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="55c42-148">Requirements</span></span>



| <span data-ttu-id="55c42-149">需求</span><span class="sxs-lookup"><span data-stu-id="55c42-149">Requirement</span></span> | <span data-ttu-id="55c42-150">值</span><span class="sxs-lookup"><span data-stu-id="55c42-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c42-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55c42-151">Minimum supported client</span></span><br/> | <span data-ttu-id="55c42-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55c42-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="55c42-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55c42-153">Minimum supported server</span></span><br/> | <span data-ttu-id="55c42-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55c42-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="55c42-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="55c42-155">Namespace</span></span><br/>                | <span data-ttu-id="55c42-156">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="55c42-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="55c42-157">MOF</span><span class="sxs-lookup"><span data-stu-id="55c42-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55c42-158"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55c42-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="55c42-159">DLL</span><span class="sxs-lookup"><span data-stu-id="55c42-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c42-160"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c42-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c42-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55c42-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c42-162">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="55c42-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
