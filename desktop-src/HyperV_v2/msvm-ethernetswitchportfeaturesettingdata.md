---
description: 類別的抽象基類，代表乙太網路交換器埠功能的設定。
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Msvm_EthernetSwitchPortFeatureSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319400"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="2853a-103">Msvm \_ EthernetSwitchPortFeatureSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="2853a-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="2853a-104">類別的抽象基類，代表乙太網路交換器埠功能的設定。</span><span class="sxs-lookup"><span data-stu-id="2853a-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="2853a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2853a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2853a-106">語法</span><span class="sxs-lookup"><span data-stu-id="2853a-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="2853a-107">成員</span><span class="sxs-lookup"><span data-stu-id="2853a-107">Members</span></span>

<span data-ttu-id="2853a-108">**Msvm \_ EthernetSwitchPortFeatureSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2853a-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2853a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2853a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2853a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2853a-110">Properties</span></span>

<span data-ttu-id="2853a-111">**Msvm \_ EthernetSwitchPortFeatureSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2853a-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2853a-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="2853a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2853a-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2853a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2853a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2853a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2853a-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="2853a-115">A short description of the object.</span></span> <span data-ttu-id="2853a-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2853a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2853a-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="2853a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2853a-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2853a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2853a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2853a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2853a-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="2853a-120">A description of the object.</span></span> <span data-ttu-id="2853a-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2853a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2853a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2853a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2853a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2853a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2853a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2853a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2853a-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2853a-125">A display name for the object.</span></span> <span data-ttu-id="2853a-126">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2853a-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2853a-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2853a-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2853a-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2853a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2853a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2853a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2853a-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="2853a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2853a-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2853a-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2853a-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2853a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2853a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2853a-133">Requirements</span></span>



| <span data-ttu-id="2853a-134">需求</span><span class="sxs-lookup"><span data-stu-id="2853a-134">Requirement</span></span> | <span data-ttu-id="2853a-135">值</span><span class="sxs-lookup"><span data-stu-id="2853a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2853a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2853a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2853a-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2853a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2853a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2853a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2853a-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2853a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2853a-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="2853a-140">Namespace</span></span><br/>                | <span data-ttu-id="2853a-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2853a-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2853a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2853a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2853a-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2853a-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2853a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2853a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2853a-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2853a-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

