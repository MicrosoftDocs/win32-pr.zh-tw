---
description: Win32 Tpm 類別的 IsEnabled 方法 \_ 會指出是否已啟用裝置。 此值可由 Enable 和 Disable 方法變更。
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Win32_Tpm 類別的 IsEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989905"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="4a9ce-104">Win32 Tpm 類別的 IsEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4a9ce-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="4a9ce-105">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsEnabled** 方法會指出是否已啟用裝置。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="4a9ce-106">此值可由 [**Enable**](enable-win32-tpm.md) 和 [**Disable**](disable-win32-tpm.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a9ce-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4a9ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a9ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a9ce-109">*IsEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a9ce-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9ce-110">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4a9ce-110">Type: **boolean**</span></span>

<span data-ttu-id="4a9ce-111">若 **為 true**，則會啟用裝置。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a9ce-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a9ce-112">Return value</span></span>

<span data-ttu-id="4a9ce-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4a9ce-113">Type: **uint32**</span></span>

<span data-ttu-id="4a9ce-114">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="4a9ce-115">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="4a9ce-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4a9ce-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4a9ce-117">Description</span><span class="sxs-lookup"><span data-stu-id="4a9ce-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4a9ce-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ce-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4a9ce-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a9ce-120">備註</span><span class="sxs-lookup"><span data-stu-id="4a9ce-120">Remarks</span></span>

<span data-ttu-id="4a9ce-121">根據受信任的運算群組 (TCG) 1.2 規格，只有在裝置處於停用狀態時，才能使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="4a9ce-122">TPM \_ ContinueSelfTest</span><span class="sxs-lookup"><span data-stu-id="4a9ce-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="4a9ce-123">TPM \_ DSAP</span><span class="sxs-lookup"><span data-stu-id="4a9ce-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="4a9ce-124">TPM \_ FlushSpecific</span><span class="sxs-lookup"><span data-stu-id="4a9ce-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="4a9ce-125">TPM \_ GetCapability</span><span class="sxs-lookup"><span data-stu-id="4a9ce-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="4a9ce-126">TPM \_ GetTestResult</span><span class="sxs-lookup"><span data-stu-id="4a9ce-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="4a9ce-127">TPM \_ 初始化</span><span class="sxs-lookup"><span data-stu-id="4a9ce-127">TPM\_Init</span></span>
-   <span data-ttu-id="4a9ce-128">TPM \_ OIAP</span><span class="sxs-lookup"><span data-stu-id="4a9ce-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="4a9ce-129">TPM \_ OSAP</span><span class="sxs-lookup"><span data-stu-id="4a9ce-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="4a9ce-130">TPM \_ OwnerSetDisable</span><span class="sxs-lookup"><span data-stu-id="4a9ce-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="4a9ce-131">TPM \_ PCR \_ 重設</span><span class="sxs-lookup"><span data-stu-id="4a9ce-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="4a9ce-132">TPM \_ PhysicalDisable</span><span class="sxs-lookup"><span data-stu-id="4a9ce-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="4a9ce-133">TPM \_ PhysicalEnable</span><span class="sxs-lookup"><span data-stu-id="4a9ce-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="4a9ce-134">TPM \_ PhysicalSetDeactivated</span><span class="sxs-lookup"><span data-stu-id="4a9ce-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="4a9ce-135">TPM \_ 重設</span><span class="sxs-lookup"><span data-stu-id="4a9ce-135">TPM\_Reset</span></span>
-   <span data-ttu-id="4a9ce-136">TPM \_ SaveState</span><span class="sxs-lookup"><span data-stu-id="4a9ce-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="4a9ce-137">TPM \_ SelfTestFull</span><span class="sxs-lookup"><span data-stu-id="4a9ce-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="4a9ce-138">TPM \_ SetCapability</span><span class="sxs-lookup"><span data-stu-id="4a9ce-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="4a9ce-139">TPM \_ SHA1Complete</span><span class="sxs-lookup"><span data-stu-id="4a9ce-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="4a9ce-140">TPM \_ SHA1Start</span><span class="sxs-lookup"><span data-stu-id="4a9ce-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="4a9ce-141">TPM \_ SHA1Update</span><span class="sxs-lookup"><span data-stu-id="4a9ce-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="4a9ce-142">TPM \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="4a9ce-142">TPM\_Startup</span></span>
-   <span data-ttu-id="4a9ce-143">TPM \_ TakeOwnership</span><span class="sxs-lookup"><span data-stu-id="4a9ce-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="4a9ce-144">TPM \_ 終止 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="4a9ce-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="4a9ce-145">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4a9ce-146">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4a9ce-147">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4a9ce-148">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="4a9ce-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a9ce-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a9ce-149">Requirements</span></span>



| <span data-ttu-id="4a9ce-150">需求</span><span class="sxs-lookup"><span data-stu-id="4a9ce-150">Requirement</span></span> | <span data-ttu-id="4a9ce-151">值</span><span class="sxs-lookup"><span data-stu-id="4a9ce-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9ce-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a9ce-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4a9ce-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a9ce-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4a9ce-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a9ce-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4a9ce-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a9ce-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a9ce-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="4a9ce-156">Namespace</span></span><br/>                | <span data-ttu-id="4a9ce-157">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="4a9ce-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="4a9ce-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4a9ce-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a9ce-159"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ce-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a9ce-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4a9ce-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a9ce-161"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a9ce-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9ce-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a9ce-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9ce-163">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="4a9ce-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="4a9ce-164">**停用**</span><span class="sxs-lookup"><span data-stu-id="4a9ce-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="4a9ce-165">**啟用**</span><span class="sxs-lookup"><span data-stu-id="4a9ce-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
