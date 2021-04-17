---
title: Win32_TerminalServiceSetting 類別的 SetPolicyPropertyName 方法
description: SetPolicyPropertyName 方法會設定類別的 DeleteTempFolders、UseTempFolders 或 Help 屬性。
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- SetPolicyPropertyName 方法遠端桌面服務
- SetPolicyPropertyName 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetPolicyPropertyName 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466717"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="71f6a-106">Win32 TerminalServiceSetting 類別的 SetPolicyPropertyName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="71f6a-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="71f6a-107">**SetPolicyPropertyName** 方法會設定類別的 **DeleteTempFolders**、 **UseTempFolders** 或 **Help** 屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f6a-108">語法</span><span class="sxs-lookup"><span data-stu-id="71f6a-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="71f6a-109">參數</span><span class="sxs-lookup"><span data-stu-id="71f6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f6a-110">*PropertyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71f6a-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f6a-111">指定方法設定的原則屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="71f6a-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="71f6a-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="71f6a-113">方法正在設定 **DeleteTempFolders** 屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="71f6a-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="71f6a-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="71f6a-115">方法正在設定 **UseTempFolders** 屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="71f6a-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**説明**</span><span class="sxs-lookup"><span data-stu-id="71f6a-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="71f6a-117">方法正在設定 **Help** 屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="71f6a-118">**注意：**  **不支援** 說明</span><span class="sxs-lookup"><span data-stu-id="71f6a-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="71f6a-119">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71f6a-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f6a-120">值，指出是否要啟用或停用 *PropertyName* 參數所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="71f6a-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="71f6a-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="71f6a-122">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="71f6a-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="71f6a-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="71f6a-124">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="71f6a-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f6a-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="71f6a-125">Return value</span></span>

<span data-ttu-id="71f6a-126">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="71f6a-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="71f6a-127">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="71f6a-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="71f6a-128">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="71f6a-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="71f6a-129">備註</span><span class="sxs-lookup"><span data-stu-id="71f6a-129">Remarks</span></span>

<span data-ttu-id="71f6a-130">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="71f6a-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="71f6a-131">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="71f6a-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="71f6a-132">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="71f6a-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="71f6a-133">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="71f6a-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="71f6a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="71f6a-134">Requirements</span></span>



| <span data-ttu-id="71f6a-135">需求</span><span class="sxs-lookup"><span data-stu-id="71f6a-135">Requirement</span></span> | <span data-ttu-id="71f6a-136">值</span><span class="sxs-lookup"><span data-stu-id="71f6a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71f6a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71f6a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="71f6a-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71f6a-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71f6a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71f6a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="71f6a-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71f6a-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71f6a-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="71f6a-141">Namespace</span></span><br/>                | <span data-ttu-id="71f6a-142">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="71f6a-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="71f6a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="71f6a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f6a-144"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="71f6a-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="71f6a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="71f6a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f6a-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71f6a-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f6a-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71f6a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f6a-148">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="71f6a-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

