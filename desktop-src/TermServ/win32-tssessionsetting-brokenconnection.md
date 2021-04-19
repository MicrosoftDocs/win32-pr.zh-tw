---
title: 'Win32_TSSessionSetting 類別的 BrokenConnection 方法 (Wtsprotocol) '
description: 設定 BrokenConnectionAction 屬性，這是當達到會話時間限制或連接中斷時，伺服器所採取的動作。
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- BrokenConnection 方法遠端桌面服務
- BrokenConnection 方法遠端桌面服務，Win32_TSSessionSetting 類別
- Win32_TSSessionSetting 類別遠端桌面服務，BrokenConnection 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966308"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="57c97-106">Win32 TSSessionSetting 類別的 BrokenConnection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="57c97-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="57c97-107">設定 **BrokenConnectionAction** 屬性，這是當達到會話時間限制或連接中斷時，伺服器所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="57c97-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="57c97-108">語法</span><span class="sxs-lookup"><span data-stu-id="57c97-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="57c97-109">參數</span><span class="sxs-lookup"><span data-stu-id="57c97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57c97-110">*BrokenConnectionAction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57c97-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c97-111">採取的動作。</span><span class="sxs-lookup"><span data-stu-id="57c97-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="57c97-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**中斷** (0) </span><span class="sxs-lookup"><span data-stu-id="57c97-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="57c97-113">使用者已與會話中斷連線。</span><span class="sxs-lookup"><span data-stu-id="57c97-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="57c97-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (1) </span><span class="sxs-lookup"><span data-stu-id="57c97-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="57c97-115">從伺服器中永久刪除會話。</span><span class="sxs-lookup"><span data-stu-id="57c97-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57c97-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="57c97-116">Return value</span></span>

<span data-ttu-id="57c97-117">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57c97-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="57c97-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="57c97-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="57c97-119">如果設定位於群組原則 control 下，方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="57c97-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="57c97-120">備註</span><span class="sxs-lookup"><span data-stu-id="57c97-120">Remarks</span></span>

<span data-ttu-id="57c97-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="57c97-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="57c97-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="57c97-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="57c97-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="57c97-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="57c97-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="57c97-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="57c97-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="57c97-125">Requirements</span></span>



| <span data-ttu-id="57c97-126">需求</span><span class="sxs-lookup"><span data-stu-id="57c97-126">Requirement</span></span> | <span data-ttu-id="57c97-127">值</span><span class="sxs-lookup"><span data-stu-id="57c97-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="57c97-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57c97-128">Minimum supported client</span></span><br/> | <span data-ttu-id="57c97-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57c97-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="57c97-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57c97-130">Minimum supported server</span></span><br/> | <span data-ttu-id="57c97-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57c97-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="57c97-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="57c97-132">Namespace</span></span><br/>                | <span data-ttu-id="57c97-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="57c97-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="57c97-134">標頭</span><span class="sxs-lookup"><span data-stu-id="57c97-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="57c97-135"><dt>Wtsprotocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="57c97-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="57c97-136">MOF</span><span class="sxs-lookup"><span data-stu-id="57c97-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57c97-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="57c97-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="57c97-138">DLL</span><span class="sxs-lookup"><span data-stu-id="57c97-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57c97-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57c97-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="57c97-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57c97-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57c97-141">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="57c97-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

