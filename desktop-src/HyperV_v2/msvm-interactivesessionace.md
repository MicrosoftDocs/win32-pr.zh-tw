---
description: 表示存取控制專案 (ACE) ，可判斷虛擬機器的互動式會話存取。
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967162"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="86e97-103">Msvm \_ InteractiveSessionACE 類別</span><span class="sxs-lookup"><span data-stu-id="86e97-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="86e97-104">表示 *存取控制專案* (ACE) ，可判斷虛擬機器的互動式會話存取。</span><span class="sxs-lookup"><span data-stu-id="86e97-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="86e97-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="86e97-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e97-106">語法</span><span class="sxs-lookup"><span data-stu-id="86e97-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="86e97-107">成員</span><span class="sxs-lookup"><span data-stu-id="86e97-107">Members</span></span>

<span data-ttu-id="86e97-108">**Msvm \_ InteractiveSessionACE** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86e97-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="86e97-109">屬性</span><span class="sxs-lookup"><span data-stu-id="86e97-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86e97-110">屬性</span><span class="sxs-lookup"><span data-stu-id="86e97-110">Properties</span></span>

<span data-ttu-id="86e97-111">**Msvm \_ InteractiveSessionACE** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86e97-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86e97-112">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="86e97-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86e97-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="86e97-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86e97-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86e97-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86e97-115">指出 ACE 是否授與或拒絕受信任者的存取權。</span><span class="sxs-lookup"><span data-stu-id="86e97-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="86e97-116">**允許存取** (0) </span><span class="sxs-lookup"><span data-stu-id="86e97-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="86e97-117">**拒絕存取** (1) </span><span class="sxs-lookup"><span data-stu-id="86e97-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86e97-118">**受託 人**</span><span class="sxs-lookup"><span data-stu-id="86e97-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86e97-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="86e97-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86e97-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86e97-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86e97-121">識別 ACE 授與或拒絕存取的安全性主體。</span><span class="sxs-lookup"><span data-stu-id="86e97-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="86e97-122">這個屬性的有效格式包括 Windows SAM 相容的使用者名稱格式和 Windows SID 字串格式。</span><span class="sxs-lookup"><span data-stu-id="86e97-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86e97-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="86e97-123">Requirements</span></span>



| <span data-ttu-id="86e97-124">需求</span><span class="sxs-lookup"><span data-stu-id="86e97-124">Requirement</span></span> | <span data-ttu-id="86e97-125">值</span><span class="sxs-lookup"><span data-stu-id="86e97-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e97-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86e97-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86e97-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86e97-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="86e97-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86e97-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86e97-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86e97-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86e97-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="86e97-130">Namespace</span></span><br/>                | <span data-ttu-id="86e97-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="86e97-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="86e97-132">MOF</span><span class="sxs-lookup"><span data-stu-id="86e97-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86e97-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="86e97-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="86e97-134">DLL</span><span class="sxs-lookup"><span data-stu-id="86e97-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e97-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86e97-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="86e97-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86e97-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e97-137">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="86e97-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




