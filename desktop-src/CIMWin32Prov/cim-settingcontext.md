---
description: CIM \_ SettingCoNtext 類別會將設定物件與設定物件建立關聯。
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingCoNtext 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936177"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="c9cfe-103">CIM \_ SettingCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="c9cfe-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="c9cfe-104">**CIM \_ SettingCoNtext** 類別會將設定物件與設定物件建立關聯。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="c9cfe-105">例如，網路介面卡的設定可能會根據其主控電腦系統所連接的網站或網路而變更。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="c9cfe-106">在這種情況下，電腦系統會有兩個不同的設定物件，對應至兩個網路區段的網路設定差異。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="c9cfe-107">其中一個設定會在一段時間進行操作時匯總網路介面卡的設定物件;相反地，另一個設定會匯總不同的網路介面卡設定物件，該物件是另一個區段特有的。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="c9cfe-108">請注意，許多電腦設定與網路設定無關。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="c9cfe-109">例如，這兩個設定會匯總電腦系統監視器解析度的相同設定物件。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9cfe-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c9cfe-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c9cfe-112">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c9cfe-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cfe-114">語法</span><span class="sxs-lookup"><span data-stu-id="c9cfe-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="c9cfe-115">成員</span><span class="sxs-lookup"><span data-stu-id="c9cfe-115">Members</span></span>

<span data-ttu-id="c9cfe-116">**CIM \_ SettingCoNtext** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9cfe-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="c9cfe-117">屬性</span><span class="sxs-lookup"><span data-stu-id="c9cfe-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9cfe-118">屬性</span><span class="sxs-lookup"><span data-stu-id="c9cfe-118">Properties</span></span>

<span data-ttu-id="c9cfe-119">**CIM \_ SettingCoNtext** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9cfe-120">**內容**</span><span class="sxs-lookup"><span data-stu-id="c9cfe-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9cfe-121">資料類型： **CIM \_** 設定</span><span class="sxs-lookup"><span data-stu-id="c9cfe-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="c9cfe-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9cfe-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9cfe-123">限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c9cfe-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c9cfe-124">參考匯總設定的設定物件。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="c9cfe-125">**設定**</span><span class="sxs-lookup"><span data-stu-id="c9cfe-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9cfe-126">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="c9cfe-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="c9cfe-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9cfe-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9cfe-128">匯總設定的參考。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9cfe-129">備註</span><span class="sxs-lookup"><span data-stu-id="c9cfe-129">Remarks</span></span>

<span data-ttu-id="c9cfe-130">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-130">WMI does not implement this class.</span></span>

<span data-ttu-id="c9cfe-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c9cfe-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c9cfe-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cfe-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9cfe-133">Requirements</span></span>



| <span data-ttu-id="c9cfe-134">需求</span><span class="sxs-lookup"><span data-stu-id="c9cfe-134">Requirement</span></span> | <span data-ttu-id="c9cfe-135">值</span><span class="sxs-lookup"><span data-stu-id="c9cfe-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cfe-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9cfe-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cfe-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9cfe-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9cfe-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9cfe-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cfe-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9cfe-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9cfe-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9cfe-140">Namespace</span></span><br/>                | <span data-ttu-id="c9cfe-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c9cfe-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9cfe-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c9cfe-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9cfe-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9cfe-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9cfe-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cfe-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cfe-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9cfe-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

