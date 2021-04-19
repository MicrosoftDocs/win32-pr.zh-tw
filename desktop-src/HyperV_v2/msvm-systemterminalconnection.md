---
description: 將虛擬機器與終端機連線建立關聯。
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973016"
---
# <a name="msvm_systemterminalconnection-class"></a><span data-ttu-id="25c0a-103">Msvm \_ SystemTerminalConnection 類別</span><span class="sxs-lookup"><span data-stu-id="25c0a-103">Msvm\_SystemTerminalConnection class</span></span>

<span data-ttu-id="25c0a-104">將虛擬機器與終端機連線建立關聯。</span><span class="sxs-lookup"><span data-stu-id="25c0a-104">Associates a virtual machine with a terminal connection.</span></span>

<span data-ttu-id="25c0a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="25c0a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c0a-106">語法</span><span class="sxs-lookup"><span data-stu-id="25c0a-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="25c0a-107">成員</span><span class="sxs-lookup"><span data-stu-id="25c0a-107">Members</span></span>

<span data-ttu-id="25c0a-108">**Msvm \_ SystemTerminalConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="25c0a-108">The **Msvm\_SystemTerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="25c0a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="25c0a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25c0a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="25c0a-110">Properties</span></span>

<span data-ttu-id="25c0a-111">**Msvm \_ SystemTerminalConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="25c0a-111">The **Msvm\_SystemTerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25c0a-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="25c0a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25c0a-113">資料類型： **[ **Msvm \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="25c0a-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="25c0a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25c0a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25c0a-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="25c0a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="25c0a-116">連接所連接的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="25c0a-116">The virtual machine to which the connection is attached.</span></span>

</dd> <dt>

<span data-ttu-id="25c0a-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="25c0a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25c0a-118">資料類型： **[ **Msvm \_ TerminalConnection**](msvm-terminalconnection.md)**</span><span class="sxs-lookup"><span data-stu-id="25c0a-118">Data type: **[**Msvm\_TerminalConnection**](msvm-terminalconnection.md)**</span></span>
</dt> <dt>

<span data-ttu-id="25c0a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="25c0a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25c0a-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="25c0a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="25c0a-121">虛擬機器的連接。</span><span class="sxs-lookup"><span data-stu-id="25c0a-121">The connection to the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25c0a-122">備註</span><span class="sxs-lookup"><span data-stu-id="25c0a-122">Remarks</span></span>

<span data-ttu-id="25c0a-123">存取 **Msvm \_ SystemTerminalConnection** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="25c0a-123">Access to the **Msvm\_SystemTerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="25c0a-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="25c0a-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="25c0a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="25c0a-125">Requirements</span></span>



| <span data-ttu-id="25c0a-126">需求</span><span class="sxs-lookup"><span data-stu-id="25c0a-126">Requirement</span></span> | <span data-ttu-id="25c0a-127">值</span><span class="sxs-lookup"><span data-stu-id="25c0a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c0a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25c0a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="25c0a-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25c0a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="25c0a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25c0a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="25c0a-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25c0a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25c0a-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="25c0a-132">Namespace</span></span><br/>                | <span data-ttu-id="25c0a-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="25c0a-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="25c0a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="25c0a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25c0a-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="25c0a-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25c0a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="25c0a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25c0a-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25c0a-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25c0a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25c0a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c0a-139">**CIM \_ HostedDependency**</span><span class="sxs-lookup"><span data-stu-id="25c0a-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="25c0a-140">[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25c0a-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="25c0a-141">影片類別</span><span class="sxs-lookup"><span data-stu-id="25c0a-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

