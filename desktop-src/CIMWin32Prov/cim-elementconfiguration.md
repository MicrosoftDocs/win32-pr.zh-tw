---
description: CIM \_ ElementConfiguration 關聯會將 cim 設定 \_ 物件與一或多個受管理的系統元素產生關聯。 CIM 設定 \_ 物件代表特定的行為，或相關聯之 CIM ManagedSystemElement 所需的功能狀態 \_ 。
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025940"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="b0a12-104">CIM \_ ElementConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="b0a12-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="b0a12-105">**Cim \_ ElementConfiguration** 關聯會將 [**cim \_ 設定**](cim-configuration.md)物件與一或多個受管理的系統元素產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b0a12-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="b0a12-106">**Cim 設定 \_** 物件代表特定的行為，或相關聯之 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)所需的功能狀態。</span><span class="sxs-lookup"><span data-stu-id="b0a12-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0a12-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b0a12-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0a12-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b0a12-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0a12-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b0a12-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b0a12-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b0a12-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a12-111">語法</span><span class="sxs-lookup"><span data-stu-id="b0a12-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="b0a12-112">成員</span><span class="sxs-lookup"><span data-stu-id="b0a12-112">Members</span></span>

<span data-ttu-id="b0a12-113">**CIM \_ ElementConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0a12-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b0a12-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b0a12-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0a12-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b0a12-115">Properties</span></span>

<span data-ttu-id="b0a12-116">**CIM \_ ElementConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b0a12-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0a12-117">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="b0a12-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a12-118">資料類型： **CIM \_** 設定</span><span class="sxs-lookup"><span data-stu-id="b0a12-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="b0a12-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0a12-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0a12-120">[**CIM \_**](cim-configuration.md)設定物件的參考，此物件會將與 managed 系統專案相關聯的設定和相依性進行分組。</span><span class="sxs-lookup"><span data-stu-id="b0a12-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="b0a12-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="b0a12-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0a12-122">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b0a12-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b0a12-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0a12-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0a12-124">Managed 系統元素的參考。</span><span class="sxs-lookup"><span data-stu-id="b0a12-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0a12-125">備註</span><span class="sxs-lookup"><span data-stu-id="b0a12-125">Remarks</span></span>

<span data-ttu-id="b0a12-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b0a12-126">WMI does not implement this class.</span></span>

<span data-ttu-id="b0a12-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b0a12-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0a12-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b0a12-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a12-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0a12-129">Requirements</span></span>



| <span data-ttu-id="b0a12-130">需求</span><span class="sxs-lookup"><span data-stu-id="b0a12-130">Requirement</span></span> | <span data-ttu-id="b0a12-131">值</span><span class="sxs-lookup"><span data-stu-id="b0a12-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a12-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0a12-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a12-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0a12-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0a12-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0a12-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a12-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0a12-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0a12-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="b0a12-136">Namespace</span></span><br/>                | <span data-ttu-id="b0a12-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b0a12-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0a12-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b0a12-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0a12-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0a12-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0a12-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b0a12-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0a12-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0a12-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




