---
description: 將兩個代表相同基礎實體不同層面的 managed 專案產生關聯。
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513360"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="e9cb6-103">Msvm \_ LogicalIdentity 類別</span><span class="sxs-lookup"><span data-stu-id="e9cb6-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="e9cb6-104">將兩個代表相同基礎實體不同層面的 managed 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="e9cb6-105">此類別衍生自 [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="e9cb6-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cb6-107">語法</span><span class="sxs-lookup"><span data-stu-id="e9cb6-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="e9cb6-108">成員</span><span class="sxs-lookup"><span data-stu-id="e9cb6-108">Members</span></span>

<span data-ttu-id="e9cb6-109">**Msvm \_ LogicalIdentity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e9cb6-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="e9cb6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e9cb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9cb6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e9cb6-111">Properties</span></span>

<span data-ttu-id="e9cb6-112">**Msvm \_ LogicalIdentity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9cb6-113">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9cb6-114">資料類型： **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e9cb6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e9cb6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9cb6-116">系統實體替代層面的參考。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="e9cb6-117">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9cb6-118">資料類型： **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e9cb6-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e9cb6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9cb6-120">邏輯元素的一個層面參考。</span><span class="sxs-lookup"><span data-stu-id="e9cb6-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9cb6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9cb6-121">Requirements</span></span>



| <span data-ttu-id="e9cb6-122">需求</span><span class="sxs-lookup"><span data-stu-id="e9cb6-122">Requirement</span></span> | <span data-ttu-id="e9cb6-123">值</span><span class="sxs-lookup"><span data-stu-id="e9cb6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cb6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9cb6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cb6-125">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9cb6-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e9cb6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9cb6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cb6-127">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9cb6-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9cb6-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9cb6-128">Namespace</span></span><br/>                | <span data-ttu-id="e9cb6-129">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e9cb6-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9cb6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e9cb6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9cb6-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e9cb6-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9cb6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e9cb6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9cb6-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9cb6-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9cb6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9cb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cb6-135">**CIM \_ LogicalIdentity**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="e9cb6-136">**CIM \_ LogicalIdentity**</span><span class="sxs-lookup"><span data-stu-id="e9cb6-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

