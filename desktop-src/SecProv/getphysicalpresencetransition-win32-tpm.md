---
description: 指出執行可信賴平臺模組 (TPM) 實體目前狀態作業所需的使用者動作。 使用 SetPhysicalPresenceRequest 方法來要求作業。
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Win32_Tpm 類別的 GetPhysicalPresenceTransition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994440"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="1d5c0-104">Win32 Tpm 類別的 GetPhysicalPresenceTransition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1d5c0-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="1d5c0-105">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **GetPhysicalPresenceTransition** 方法表示執行信賴平臺模組所需的使用者動作 (Tpm) 實體目前狀態作業。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="1d5c0-106">使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="1d5c0-107">製造時，會為您的電腦設定必要的使用者動作。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="1d5c0-108">通常需要重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5c0-109">語法</span><span class="sxs-lookup"><span data-stu-id="1d5c0-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="1d5c0-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d5c0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5c0-111">*轉換* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d5c0-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5c0-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1d5c0-112">Type: **uint32**</span></span>

<span data-ttu-id="1d5c0-113">整數值，指定執行 TPM 實體存在作業所需的轉換。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="1d5c0-114">值</span><span class="sxs-lookup"><span data-stu-id="1d5c0-114">Value</span></span>                                                                        | <span data-ttu-id="1d5c0-115">意義</span><span class="sxs-lookup"><span data-stu-id="1d5c0-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d5c0-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1d5c0-117">不需要採取任何使用者動作，就能執行 TPM 實體目前狀態作業。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="1d5c0-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1d5c0-119">若要執行 TPM 實體存在作業，使用者必須關閉電腦，然後使用 [電源] 按鈕將它重新開啟。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="1d5c0-120">使用者必須實際存在於電腦上，才能在 BIOS 提示時接受或拒絕變更。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="1d5c0-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1d5c0-122">若要執行 TPM 實體存在作業，使用者必須使用熱重新開機來重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="1d5c0-123">使用者必須實際存在於電腦上，才能在 BIOS 提示時接受或拒絕變更。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="1d5c0-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1d5c0-125">必要的使用者動作未知。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d5c0-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d5c0-126">Return value</span></span>

<span data-ttu-id="1d5c0-127">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1d5c0-127">Type: **uint32**</span></span>

<span data-ttu-id="1d5c0-128">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="1d5c0-129">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="1d5c0-130">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1d5c0-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="1d5c0-131">Description</span><span class="sxs-lookup"><span data-stu-id="1d5c0-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d5c0-132"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="1d5c0-133">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="1d5c0-134"><dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="1d5c0-135">發生硬體故障。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-135">A hardware failure occurred.</span></span> <span data-ttu-id="1d5c0-136">如需詳細資訊，請洽詢您的電腦製造商。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d5c0-137">備註</span><span class="sxs-lookup"><span data-stu-id="1d5c0-137">Remarks</span></span>

<span data-ttu-id="1d5c0-138">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1d5c0-139">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1d5c0-140">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1d5c0-141">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1d5c0-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5c0-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d5c0-142">Requirements</span></span>



| <span data-ttu-id="1d5c0-143">需求</span><span class="sxs-lookup"><span data-stu-id="1d5c0-143">Requirement</span></span> | <span data-ttu-id="1d5c0-144">值</span><span class="sxs-lookup"><span data-stu-id="1d5c0-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5c0-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d5c0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5c0-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5c0-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1d5c0-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d5c0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5c0-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5c0-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1d5c0-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d5c0-149">Namespace</span></span><br/>                | <span data-ttu-id="1d5c0-150">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="1d5c0-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="1d5c0-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1d5c0-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d5c0-152"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d5c0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5c0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d5c0-154"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c0-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5c0-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d5c0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5c0-156">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="1d5c0-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="1d5c0-157">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="1d5c0-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
