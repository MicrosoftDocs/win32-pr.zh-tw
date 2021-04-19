---
title: Win32_TSClientSetting 類別的 SetClientProperty 方法
description: SetClientProperty 方法會設定類別的 LPTPortMapping、COMPortMapping、AudioMapping、ClipboardMapping、DriveMapping 或 WindowsPrinterMapping 屬性。
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- SetClientProperty 方法遠端桌面服務
- SetClientProperty 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetClientProperty 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967729"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="fa351-106">Win32 TSClientSetting 類別的 SetClientProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fa351-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="fa351-107">**SetClientProperty** 方法會設定類別的 **LPTPortMapping**、 **COMPortMapping**、 **AudioMapping**、 **ClipboardMapping**、 **DriveMapping** 或 **WindowsPrinterMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa351-108">語法</span><span class="sxs-lookup"><span data-stu-id="fa351-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="fa351-109">參數</span><span class="sxs-lookup"><span data-stu-id="fa351-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa351-110">*PropertyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa351-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa351-111">指定方法設定的用戶端屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="fa351-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-113">方法正在設定 **AudioMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="fa351-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-115">方法正在設定 **ClipboardMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="fa351-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-117">方法正在設定 **COMPortMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="fa351-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-119">方法正在設定 **DriveMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="fa351-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-121">方法正在設定 **LPTPortMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="fa351-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="fa351-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-123">方法正在設定 **PNPRedirection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="fa351-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="fa351-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-125">方法正在設定 **WindowsPrinterMapping** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fa351-126">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa351-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa351-127">值，指出是否要啟用或停用 *PropertyName* 參數所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="fa351-128"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="fa351-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-129">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="fa351-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fa351-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fa351-131">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="fa351-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa351-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa351-132">Return value</span></span>

<span data-ttu-id="fa351-133">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fa351-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fa351-134">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="fa351-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="fa351-135">如果指定的用戶端屬性不在群組原則控制之下，或屬性設定不符合伺服器覆寫的資格，則此方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa351-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa351-136">備註</span><span class="sxs-lookup"><span data-stu-id="fa351-136">Remarks</span></span>

<span data-ttu-id="fa351-137">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fa351-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fa351-138">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa351-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fa351-139">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fa351-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fa351-140">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="fa351-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa351-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa351-141">Requirements</span></span>



| <span data-ttu-id="fa351-142">需求</span><span class="sxs-lookup"><span data-stu-id="fa351-142">Requirement</span></span> | <span data-ttu-id="fa351-143">值</span><span class="sxs-lookup"><span data-stu-id="fa351-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa351-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa351-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fa351-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa351-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa351-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa351-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fa351-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa351-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa351-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa351-148">Namespace</span></span><br/>                | <span data-ttu-id="fa351-149">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="fa351-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fa351-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fa351-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa351-151"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa351-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa351-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fa351-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa351-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa351-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa351-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa351-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa351-155">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="fa351-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

