---
description: CIM \_ LogicalIdentity 類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: 'CIM_LogicalIdentity 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936155"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="99ffa-103">CIM_LogicalIdentity 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="99ffa-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="99ffa-104">**CIM \_ LogicalIdentity** 類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。</span><span class="sxs-lookup"><span data-stu-id="99ffa-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="99ffa-105">此關聯會傳達可使用多個繼承定義的內容，並且限制為 managed 系統專案的邏輯部分。</span><span class="sxs-lookup"><span data-stu-id="99ffa-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="99ffa-106">在大部分的情況下，識別關聯性是由索引鍵的相等或相關專案的其他一些識別屬性所決定。</span><span class="sxs-lookup"><span data-stu-id="99ffa-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="99ffa-107">關聯應僅用於已清楚瞭解的案例中，在子類別中允許更明確的定義和澄清。</span><span class="sxs-lookup"><span data-stu-id="99ffa-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="99ffa-108">以合理的關聯性為例，例如，表示同時為匯流排實體的裝置，以及裝置為 USB (匯流排) 和鍵盤 (功能) 實體的功能實體。</span><span class="sxs-lookup"><span data-stu-id="99ffa-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99ffa-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="99ffa-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99ffa-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="99ffa-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="99ffa-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="99ffa-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="99ffa-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="99ffa-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ffa-113">語法</span><span class="sxs-lookup"><span data-stu-id="99ffa-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="99ffa-114">成員</span><span class="sxs-lookup"><span data-stu-id="99ffa-114">Members</span></span>

<span data-ttu-id="99ffa-115">**CIM \_ LogicalIdentity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="99ffa-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="99ffa-116">屬性</span><span class="sxs-lookup"><span data-stu-id="99ffa-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99ffa-117">屬性</span><span class="sxs-lookup"><span data-stu-id="99ffa-117">Properties</span></span>

<span data-ttu-id="99ffa-118">**CIM \_ LogicalIdentity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99ffa-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99ffa-119">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="99ffa-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99ffa-120">資料類型： **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="99ffa-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="99ffa-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99ffa-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99ffa-122">系統實體替代層面的參考。</span><span class="sxs-lookup"><span data-stu-id="99ffa-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="99ffa-123">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="99ffa-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99ffa-124">資料類型： **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="99ffa-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="99ffa-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99ffa-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99ffa-126">邏輯元素的一個層面參考。</span><span class="sxs-lookup"><span data-stu-id="99ffa-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99ffa-127">備註</span><span class="sxs-lookup"><span data-stu-id="99ffa-127">Remarks</span></span>

<span data-ttu-id="99ffa-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="99ffa-128">WMI does not implement this class.</span></span> <span data-ttu-id="99ffa-129">針對衍生自 **CIM \_ LogicalIdentity** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="99ffa-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="99ffa-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="99ffa-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99ffa-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="99ffa-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ffa-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="99ffa-132">Requirements</span></span>



| <span data-ttu-id="99ffa-133">需求</span><span class="sxs-lookup"><span data-stu-id="99ffa-133">Requirement</span></span> | <span data-ttu-id="99ffa-134">值</span><span class="sxs-lookup"><span data-stu-id="99ffa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99ffa-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99ffa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="99ffa-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99ffa-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99ffa-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99ffa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="99ffa-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99ffa-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99ffa-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="99ffa-139">Namespace</span></span><br/>                | <span data-ttu-id="99ffa-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="99ffa-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99ffa-141">MOF</span><span class="sxs-lookup"><span data-stu-id="99ffa-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99ffa-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="99ffa-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99ffa-143">DLL</span><span class="sxs-lookup"><span data-stu-id="99ffa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ffa-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99ffa-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




