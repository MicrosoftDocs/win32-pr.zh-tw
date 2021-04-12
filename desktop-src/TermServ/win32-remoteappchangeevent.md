---
title: Win32_RemoteAppChangeEvent 類別
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) Server 上 Windows Server 2008 R2 RemoteApp 設定的變更。
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Win32_RemoteAppChangeEvent 類別遠端桌面服務
- Win32_RemoteAppChangeEvent 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103674"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="13b7d-105">Win32 \_ RemoteAppChangeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="13b7d-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="13b7d-106">代表遠端桌面工作階段主機 (RD 工作階段主機) Server 上 Windows Server 2008 R2 RemoteApp 設定的變更。</span><span class="sxs-lookup"><span data-stu-id="13b7d-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="13b7d-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="13b7d-108">成員</span><span class="sxs-lookup"><span data-stu-id="13b7d-108">Members</span></span>

<span data-ttu-id="13b7d-109">**Win32 \_ RemoteAppChangeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13b7d-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="13b7d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="13b7d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13b7d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="13b7d-111">Properties</span></span>

<span data-ttu-id="13b7d-112">**Win32 \_ RemoteAppChangeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13b7d-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13b7d-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="13b7d-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b7d-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="13b7d-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="13b7d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13b7d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13b7d-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="13b7d-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="13b7d-117">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="13b7d-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="13b7d-118">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。</span><span class="sxs-lookup"><span data-stu-id="13b7d-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="13b7d-119">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="13b7d-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b7d-120">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="13b7d-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13b7d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13b7d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13b7d-122">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="13b7d-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="13b7d-123">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="13b7d-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="13b7d-124">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="13b7d-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="13b7d-125">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="13b7d-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="13b7d-126">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="13b7d-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13b7d-127">備註</span><span class="sxs-lookup"><span data-stu-id="13b7d-127">Remarks</span></span>

<span data-ttu-id="13b7d-128">若要連接到「根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway」命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="13b7d-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="13b7d-129">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="13b7d-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="13b7d-130">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="13b7d-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="13b7d-131">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="13b7d-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="13b7d-132">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="13b7d-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="13b7d-133">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="13b7d-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="13b7d-134">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="13b7d-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="13b7d-135">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="13b7d-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="13b7d-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="13b7d-136">Requirements</span></span>



| <span data-ttu-id="13b7d-137">需求</span><span class="sxs-lookup"><span data-stu-id="13b7d-137">Requirement</span></span> | <span data-ttu-id="13b7d-138">值</span><span class="sxs-lookup"><span data-stu-id="13b7d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13b7d-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13b7d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="13b7d-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="13b7d-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="13b7d-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13b7d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="13b7d-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13b7d-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13b7d-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="13b7d-143">Namespace</span></span><br/>                | <span data-ttu-id="13b7d-144">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="13b7d-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="13b7d-145">MOF</span><span class="sxs-lookup"><span data-stu-id="13b7d-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b7d-146"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="13b7d-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="13b7d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="13b7d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b7d-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b7d-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

