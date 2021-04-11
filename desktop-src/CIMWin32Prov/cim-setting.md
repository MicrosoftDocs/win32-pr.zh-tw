---
description: CIM \_ 設定類別代表一或多個受管理系統元素的設定相關和指令引數。
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: 'CIM_Setting 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847242"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="e3917-103">CIM_Setting 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="e3917-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e3917-104">**CIM \_ 設定** 類別代表一或多個受管理系統元素的設定相關和指令引數。</span><span class="sxs-lookup"><span data-stu-id="e3917-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="e3917-105">受管理的系統專案可以有多個相關聯的設定物件。</span><span class="sxs-lookup"><span data-stu-id="e3917-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="e3917-106">專案參數的目前操作值會由專案本身中的屬性或其關聯中的屬性所反映。</span><span class="sxs-lookup"><span data-stu-id="e3917-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="e3917-107">這些屬性不一定要存在於設定物件中的相同值。</span><span class="sxs-lookup"><span data-stu-id="e3917-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="e3917-108">例如，數據機的設定速率可能是每秒 56 kb，但以每秒 19.2 kb 的速度運作。</span><span class="sxs-lookup"><span data-stu-id="e3917-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3917-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e3917-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e3917-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e3917-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e3917-111">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3917-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e3917-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e3917-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3917-113">語法</span><span class="sxs-lookup"><span data-stu-id="e3917-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="e3917-114">成員</span><span class="sxs-lookup"><span data-stu-id="e3917-114">Members</span></span>

<span data-ttu-id="e3917-115">**CIM \_ 設定** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e3917-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="e3917-116">屬性</span><span class="sxs-lookup"><span data-stu-id="e3917-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3917-117">屬性</span><span class="sxs-lookup"><span data-stu-id="e3917-117">Properties</span></span>

<span data-ttu-id="e3917-118">**CIM \_ 設定** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e3917-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3917-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="e3917-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3917-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3917-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3917-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3917-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3917-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e3917-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e3917-123">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e3917-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="e3917-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="e3917-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3917-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3917-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3917-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3917-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3917-127">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="e3917-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="e3917-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e3917-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3917-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3917-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3917-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3917-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3917-131">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e3917-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e3917-132">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3917-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3917-133">備註</span><span class="sxs-lookup"><span data-stu-id="e3917-133">Remarks</span></span>

<span data-ttu-id="e3917-134">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e3917-134">WMI does not implement this class.</span></span> <span data-ttu-id="e3917-135">針對衍生自 **CIM \_ 設定** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="e3917-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e3917-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e3917-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e3917-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e3917-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3917-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3917-138">Requirements</span></span>



| <span data-ttu-id="e3917-139">需求</span><span class="sxs-lookup"><span data-stu-id="e3917-139">Requirement</span></span> | <span data-ttu-id="e3917-140">值</span><span class="sxs-lookup"><span data-stu-id="e3917-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3917-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3917-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e3917-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3917-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3917-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3917-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e3917-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3917-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3917-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3917-145">Namespace</span></span><br/>                | <span data-ttu-id="e3917-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3917-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3917-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e3917-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3917-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3917-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3917-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e3917-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3917-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3917-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

