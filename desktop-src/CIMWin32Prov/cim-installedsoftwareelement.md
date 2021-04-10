---
description: CIM \_ InstalledSoftwareElement 類別會將電腦系統與已安裝的軟體元素建立關聯。
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: CIM_InstalledSoftwareElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110844"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="bf300-103">CIM \_ InstalledSoftwareElement 類別</span><span class="sxs-lookup"><span data-stu-id="bf300-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="bf300-104">**CIM \_ InstalledSoftwareElement** 類別會將電腦系統與已安裝的軟體元素建立關聯。</span><span class="sxs-lookup"><span data-stu-id="bf300-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf300-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="bf300-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bf300-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="bf300-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bf300-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf300-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bf300-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bf300-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf300-109">語法</span><span class="sxs-lookup"><span data-stu-id="bf300-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="bf300-110">成員</span><span class="sxs-lookup"><span data-stu-id="bf300-110">Members</span></span>

<span data-ttu-id="bf300-111">**CIM \_ InstalledSoftwareElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf300-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="bf300-112">屬性</span><span class="sxs-lookup"><span data-stu-id="bf300-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf300-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bf300-113">Properties</span></span>

<span data-ttu-id="bf300-114">**CIM \_ InstalledSoftwareElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf300-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf300-115">**軟體**</span><span class="sxs-lookup"><span data-stu-id="bf300-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf300-116">資料類型： **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="bf300-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="bf300-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf300-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf300-118">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) </span><span class="sxs-lookup"><span data-stu-id="bf300-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="bf300-119">電腦系統上所安裝之 software 元素的參考。</span><span class="sxs-lookup"><span data-stu-id="bf300-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="bf300-120">**系統**</span><span class="sxs-lookup"><span data-stu-id="bf300-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf300-121">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="bf300-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bf300-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf300-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf300-123">限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) </span><span class="sxs-lookup"><span data-stu-id="bf300-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="bf300-124">參考裝載特定軟體元素的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="bf300-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf300-125">備註</span><span class="sxs-lookup"><span data-stu-id="bf300-125">Remarks</span></span>

<span data-ttu-id="bf300-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="bf300-126">WMI does not implement this class.</span></span> <span data-ttu-id="bf300-127">針對衍生自 **CIM \_ InstalledSoftwareElement** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="bf300-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bf300-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="bf300-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bf300-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bf300-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf300-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf300-130">Requirements</span></span>



| <span data-ttu-id="bf300-131">需求</span><span class="sxs-lookup"><span data-stu-id="bf300-131">Requirement</span></span> | <span data-ttu-id="bf300-132">值</span><span class="sxs-lookup"><span data-stu-id="bf300-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf300-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf300-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bf300-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf300-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf300-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf300-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bf300-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf300-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf300-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf300-137">Namespace</span></span><br/>                | <span data-ttu-id="bf300-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bf300-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf300-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bf300-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf300-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf300-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf300-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bf300-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf300-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf300-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

