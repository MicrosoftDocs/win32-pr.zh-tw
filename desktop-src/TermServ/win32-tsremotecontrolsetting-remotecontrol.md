---
title: Win32_TSRemoteControlSetting 類別的 RemoteControl 方法
description: RemoteControl 方法會設定 LevelOfControl 屬性。
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- RemoteControl 方法遠端桌面服務
- RemoteControl 方法遠端桌面服務，Win32_TSRemoteControlSetting 類別
- Win32_TSRemoteControlSetting 類別遠端桌面服務，RemoteControl 方法
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317228"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="8500d-106">Win32 TSRemoteControlSetting 類別的 RemoteControl 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8500d-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="8500d-107">**RemoteControl** 方法會設定 **LevelOfControl** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8500d-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8500d-108">語法</span><span class="sxs-lookup"><span data-stu-id="8500d-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="8500d-109">參數</span><span class="sxs-lookup"><span data-stu-id="8500d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8500d-110">*LevelOfControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8500d-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8500d-111">**LevelOfControl** 屬性的新值，這個值會指定是否只由遠端使用者查看會話，或透過鍵盤和滑鼠來查看和控制會話。</span><span class="sxs-lookup"><span data-stu-id="8500d-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="8500d-112">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="8500d-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="8500d-113">支援下列值。</span><span class="sxs-lookup"><span data-stu-id="8500d-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="8500d-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (0) </span><span class="sxs-lookup"><span data-stu-id="8500d-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8500d-115">遠端控制已停用。</span><span class="sxs-lookup"><span data-stu-id="8500d-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="8500d-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1) </span><span class="sxs-lookup"><span data-stu-id="8500d-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8500d-117">遠端控制的使用者可以完全掌控使用者的會話，以及使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="8500d-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="8500d-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2) </span><span class="sxs-lookup"><span data-stu-id="8500d-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8500d-119">遠端控制的使用者可以完全掌控使用者的會話;不需要使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="8500d-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="8500d-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3) </span><span class="sxs-lookup"><span data-stu-id="8500d-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8500d-121">遠端控制的使用者可以從遠端使用使用者的許可權來查看會話;遠端使用者無法主動控制會話。</span><span class="sxs-lookup"><span data-stu-id="8500d-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="8500d-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4) </span><span class="sxs-lookup"><span data-stu-id="8500d-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8500d-123">遠端控制的使用者可以從遠端查看會話，但不能主動控制會話;不需要使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="8500d-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8500d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="8500d-124">Return value</span></span>

<span data-ttu-id="8500d-125">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8500d-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8500d-126">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="8500d-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8500d-127">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8500d-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8500d-128">備註</span><span class="sxs-lookup"><span data-stu-id="8500d-128">Remarks</span></span>

<span data-ttu-id="8500d-129">會話的完整控制權表示遠端使用者可以使用鍵盤和滑鼠主動控制使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="8500d-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="8500d-130">當使用者嘗試建立遠端控制連線時，系統會顯示訊息給遠端用戶端，要求許可權，以在遠端會話中進行 view 或積極參與。</span><span class="sxs-lookup"><span data-stu-id="8500d-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="8500d-131">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8500d-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8500d-132">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8500d-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8500d-133">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8500d-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8500d-134">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="8500d-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8500d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8500d-135">Requirements</span></span>



| <span data-ttu-id="8500d-136">需求</span><span class="sxs-lookup"><span data-stu-id="8500d-136">Requirement</span></span> | <span data-ttu-id="8500d-137">值</span><span class="sxs-lookup"><span data-stu-id="8500d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8500d-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8500d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8500d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8500d-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8500d-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8500d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8500d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8500d-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8500d-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="8500d-142">Namespace</span></span><br/>                | <span data-ttu-id="8500d-143">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8500d-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8500d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8500d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8500d-145"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="8500d-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8500d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8500d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8500d-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8500d-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8500d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8500d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8500d-149">**Win32 \_ TSRemoteControlSetting**</span><span class="sxs-lookup"><span data-stu-id="8500d-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

