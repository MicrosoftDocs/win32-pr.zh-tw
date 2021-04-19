---
description: 用來將實例 CIM \_ RegisteredProfile 與 \_ 另一個參考相依設定檔的另一個設定檔的 cim RegisteredProfile 實例相關聯，做為相關的設定檔。
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997890"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="37ba4-103">CIM \_ ReferencedProfile 類別</span><span class="sxs-lookup"><span data-stu-id="37ba4-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="37ba4-104">用來將實例 [**cim \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 與另一個參考相依設定檔的另一個設定檔的 **cim \_ RegisteredProfile** 實例相關聯，做為相關的設定檔。</span><span class="sxs-lookup"><span data-stu-id="37ba4-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37ba4-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="37ba4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37ba4-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="37ba4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="37ba4-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="37ba4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ba4-108">語法</span><span class="sxs-lookup"><span data-stu-id="37ba4-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="37ba4-109">成員</span><span class="sxs-lookup"><span data-stu-id="37ba4-109">Members</span></span>

<span data-ttu-id="37ba4-110">**CIM \_ ReferencedProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37ba4-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="37ba4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="37ba4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37ba4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="37ba4-112">Properties</span></span>

<span data-ttu-id="37ba4-113">**CIM \_ ReferencedProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="37ba4-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37ba4-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="37ba4-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ba4-115">資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="37ba4-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="37ba4-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37ba4-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37ba4-117">指定 **相依** 設定檔所參考的 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))實例。</span><span class="sxs-lookup"><span data-stu-id="37ba4-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="37ba4-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="37ba4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ba4-119">資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="37ba4-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="37ba4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37ba4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37ba4-121">指定參考其他設定檔的 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 實例。</span><span class="sxs-lookup"><span data-stu-id="37ba4-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37ba4-122">備註</span><span class="sxs-lookup"><span data-stu-id="37ba4-122">Remarks</span></span>

<span data-ttu-id="37ba4-123">系統會定義 **CIM \_ ReferencedProfile** 關聯中的 **相依** 和 **Antecedent** 屬性，讓參考的設定檔是前一個，而執行參考的設定檔是相依的。</span><span class="sxs-lookup"><span data-stu-id="37ba4-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="37ba4-124">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="37ba4-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37ba4-125">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="37ba4-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ba4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ba4-126">Requirements</span></span>



| <span data-ttu-id="37ba4-127">需求</span><span class="sxs-lookup"><span data-stu-id="37ba4-127">Requirement</span></span> | <span data-ttu-id="37ba4-128">值</span><span class="sxs-lookup"><span data-stu-id="37ba4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ba4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37ba4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="37ba4-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37ba4-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="37ba4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37ba4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="37ba4-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37ba4-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="37ba4-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="37ba4-133">Namespace</span></span><br/>                | <span data-ttu-id="37ba4-134">根 \\ interop</span><span class="sxs-lookup"><span data-stu-id="37ba4-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="37ba4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="37ba4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37ba4-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37ba4-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37ba4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37ba4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ba4-138">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="37ba4-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

