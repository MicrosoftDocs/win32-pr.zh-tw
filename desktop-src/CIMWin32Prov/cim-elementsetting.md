---
description: CIM \_ ElementSetting 類別代表 managed 系統專案與其定義的設定類別之間的關聯。
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: 'CIM_ElementSetting 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979713"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="dfd33-103">CIM_ElementSetting 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="dfd33-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dfd33-104">**CIM \_ ElementSetting** 類別代表 managed 系統專案與其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="dfd33-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfd33-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="dfd33-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dfd33-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="dfd33-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dfd33-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dfd33-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dfd33-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dfd33-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd33-109">語法</span><span class="sxs-lookup"><span data-stu-id="dfd33-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="dfd33-110">成員</span><span class="sxs-lookup"><span data-stu-id="dfd33-110">Members</span></span>

<span data-ttu-id="dfd33-111">**CIM \_ ElementSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dfd33-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="dfd33-112">屬性</span><span class="sxs-lookup"><span data-stu-id="dfd33-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfd33-113">屬性</span><span class="sxs-lookup"><span data-stu-id="dfd33-113">Properties</span></span>

<span data-ttu-id="dfd33-114">**CIM \_ ElementSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dfd33-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfd33-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="dfd33-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfd33-116">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="dfd33-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="dfd33-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfd33-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfd33-118">**Cim \_ ElementSetting** 關聯之 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件角色的參考。</span><span class="sxs-lookup"><span data-stu-id="dfd33-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="dfd33-119">相關聯的 managed system 元素提供可執行專案設定的元素。</span><span class="sxs-lookup"><span data-stu-id="dfd33-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="dfd33-120">**設定**</span><span class="sxs-lookup"><span data-stu-id="dfd33-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfd33-121">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="dfd33-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="dfd33-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dfd33-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfd33-123">**Cim \_ ElementSetting** 關聯之 [**cim \_ 設定**](cim-setting.md)物件角色的參考。</span><span class="sxs-lookup"><span data-stu-id="dfd33-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="dfd33-124">相關聯的設定提供可執行元素設定的設定。</span><span class="sxs-lookup"><span data-stu-id="dfd33-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfd33-125">備註</span><span class="sxs-lookup"><span data-stu-id="dfd33-125">Remarks</span></span>

<span data-ttu-id="dfd33-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="dfd33-126">WMI does not implement this class.</span></span> <span data-ttu-id="dfd33-127">針對衍生自 **CIM \_ ElementSetting** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dfd33-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dfd33-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="dfd33-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dfd33-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dfd33-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd33-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfd33-130">Requirements</span></span>



| <span data-ttu-id="dfd33-131">需求</span><span class="sxs-lookup"><span data-stu-id="dfd33-131">Requirement</span></span> | <span data-ttu-id="dfd33-132">值</span><span class="sxs-lookup"><span data-stu-id="dfd33-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd33-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfd33-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd33-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfd33-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfd33-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfd33-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd33-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfd33-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfd33-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfd33-137">Namespace</span></span><br/>                | <span data-ttu-id="dfd33-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfd33-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfd33-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dfd33-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfd33-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfd33-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfd33-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd33-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd33-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd33-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




