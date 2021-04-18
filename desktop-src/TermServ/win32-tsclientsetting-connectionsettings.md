---
title: Win32_TSClientSetting 類別的 ConnectionSettings 方法
description: ConnectionSettings 方法會設定適用于連接和登入程式的會話設定。
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- ConnectionSettings 方法遠端桌面服務
- ConnectionSettings 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，ConnectionSettings 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508507"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="e95df-106">Win32 TSClientSetting 類別的 ConnectionSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e95df-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="e95df-107">**ConnectionSettings** 方法會設定適用于連接和登入程式的會話設定。</span><span class="sxs-lookup"><span data-stu-id="e95df-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95df-108">語法</span><span class="sxs-lookup"><span data-stu-id="e95df-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="e95df-109">參數</span><span class="sxs-lookup"><span data-stu-id="e95df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95df-110">*ConnectClientDrivesAtLogon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e95df-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95df-111">旗標：啟用或停用 **ConnectClientDrivesAtLogon** 屬性，指定在登入程式期間是否自動連接用戶端的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e95df-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e95df-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="e95df-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-113">用戶端的磁片磁碟機不會自動連線。</span><span class="sxs-lookup"><span data-stu-id="e95df-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="e95df-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e95df-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-115">用戶端的磁片磁碟機會自動連接。</span><span class="sxs-lookup"><span data-stu-id="e95df-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e95df-116">*ConnectPrinterAtLogon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e95df-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95df-117">旗標：啟用或停用 **ConnectPrinterAtLogon** 屬性，指定在登入程式期間是否會自動連接所有對應的本機用戶端印表機。</span><span class="sxs-lookup"><span data-stu-id="e95df-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e95df-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="e95df-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-119">所有對應的本機印表機都不會自動連接。</span><span class="sxs-lookup"><span data-stu-id="e95df-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="e95df-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e95df-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-121">所有對應的本機印表機都會自動連接。</span><span class="sxs-lookup"><span data-stu-id="e95df-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e95df-122">*DefaultToClientPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e95df-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95df-123">旗標：啟用或停用 **DefaultToClientPrinter** 屬性，指定列印工作是否自動傳送至用戶端的本機印表機。</span><span class="sxs-lookup"><span data-stu-id="e95df-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e95df-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="e95df-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-125">列印工作不會自動傳送。</span><span class="sxs-lookup"><span data-stu-id="e95df-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="e95df-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e95df-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e95df-127">列印工作會自動傳送。</span><span class="sxs-lookup"><span data-stu-id="e95df-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95df-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="e95df-128">Return value</span></span>

<span data-ttu-id="e95df-129">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e95df-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e95df-130">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="e95df-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e95df-131">如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e95df-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="e95df-132">備註</span><span class="sxs-lookup"><span data-stu-id="e95df-132">Remarks</span></span>

<span data-ttu-id="e95df-133">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e95df-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e95df-134">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e95df-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e95df-135">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e95df-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e95df-136">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e95df-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e95df-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="e95df-137">Requirements</span></span>



| <span data-ttu-id="e95df-138">需求</span><span class="sxs-lookup"><span data-stu-id="e95df-138">Requirement</span></span> | <span data-ttu-id="e95df-139">值</span><span class="sxs-lookup"><span data-stu-id="e95df-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e95df-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e95df-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e95df-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e95df-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e95df-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e95df-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e95df-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e95df-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e95df-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="e95df-144">Namespace</span></span><br/>                | <span data-ttu-id="e95df-145">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e95df-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e95df-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e95df-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e95df-147"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e95df-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e95df-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e95df-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e95df-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e95df-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e95df-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e95df-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95df-151">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="e95df-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

