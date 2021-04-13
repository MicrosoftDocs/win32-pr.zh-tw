---
description: 抽象類別，表示系統或元件之特定功能的設定。
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Msvm_FeatureSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511007"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="7124d-103">Msvm \_ FeatureSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="7124d-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="7124d-104">抽象類別，表示系統或元件之特定功能的設定。</span><span class="sxs-lookup"><span data-stu-id="7124d-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="7124d-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7124d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7124d-106">語法</span><span class="sxs-lookup"><span data-stu-id="7124d-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="7124d-107">成員</span><span class="sxs-lookup"><span data-stu-id="7124d-107">Members</span></span>

<span data-ttu-id="7124d-108">**Msvm \_ FeatureSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7124d-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7124d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7124d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7124d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7124d-110">Properties</span></span>

<span data-ttu-id="7124d-111">**Msvm \_ FeatureSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7124d-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7124d-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="7124d-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7124d-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7124d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7124d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7124d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7124d-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="7124d-115">A short description of the object.</span></span> <span data-ttu-id="7124d-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7124d-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7124d-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="7124d-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7124d-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7124d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7124d-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7124d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7124d-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7124d-120">A description of the object.</span></span> <span data-ttu-id="7124d-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7124d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7124d-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7124d-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7124d-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7124d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7124d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7124d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7124d-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7124d-125">A display name for the object.</span></span> <span data-ttu-id="7124d-126">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7124d-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7124d-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7124d-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7124d-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7124d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7124d-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7124d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7124d-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="7124d-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7124d-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7124d-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7124d-132">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7124d-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7124d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7124d-133">Requirements</span></span>



| <span data-ttu-id="7124d-134">需求</span><span class="sxs-lookup"><span data-stu-id="7124d-134">Requirement</span></span> | <span data-ttu-id="7124d-135">值</span><span class="sxs-lookup"><span data-stu-id="7124d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7124d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7124d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7124d-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7124d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7124d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7124d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7124d-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7124d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7124d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="7124d-140">Namespace</span></span><br/>                | <span data-ttu-id="7124d-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7124d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7124d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7124d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7124d-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7124d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7124d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7124d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7124d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7124d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

