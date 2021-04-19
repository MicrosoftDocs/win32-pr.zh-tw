---
description: 抽象類別，表示乙太網路交換器功能之指定實例的設定。
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Msvm_EthernetSwitchFeatureSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992618"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="aba1a-103">Msvm \_ EthernetSwitchFeatureSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="aba1a-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="aba1a-104">抽象類別，表示乙太網路交換器功能之指定實例的設定。</span><span class="sxs-lookup"><span data-stu-id="aba1a-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="aba1a-105">乙太網路交換器功能設定管理類別必須衍生自這個抽象類別。</span><span class="sxs-lookup"><span data-stu-id="aba1a-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="aba1a-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aba1a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="aba1a-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="aba1a-108">成員</span><span class="sxs-lookup"><span data-stu-id="aba1a-108">Members</span></span>

<span data-ttu-id="aba1a-109">**Msvm \_ EthernetSwitchFeatureSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aba1a-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="aba1a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aba1a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aba1a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="aba1a-111">Properties</span></span>

<span data-ttu-id="aba1a-112">**Msvm \_ EthernetSwitchFeatureSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aba1a-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aba1a-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="aba1a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1a-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aba1a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aba1a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aba1a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aba1a-116">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="aba1a-116">A short description of the object.</span></span> <span data-ttu-id="aba1a-117">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="aba1a-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aba1a-118">**說明**</span><span class="sxs-lookup"><span data-stu-id="aba1a-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1a-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aba1a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aba1a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aba1a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aba1a-121">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="aba1a-121">A description of the object.</span></span> <span data-ttu-id="aba1a-122">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="aba1a-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aba1a-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="aba1a-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1a-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aba1a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aba1a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aba1a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aba1a-126">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="aba1a-126">A display name for the object.</span></span> <span data-ttu-id="aba1a-127">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="aba1a-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="aba1a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aba1a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aba1a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aba1a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aba1a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aba1a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aba1a-131">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="aba1a-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="aba1a-132">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="aba1a-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="aba1a-133">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="aba1a-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aba1a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="aba1a-134">Requirements</span></span>



| <span data-ttu-id="aba1a-135">需求</span><span class="sxs-lookup"><span data-stu-id="aba1a-135">Requirement</span></span> | <span data-ttu-id="aba1a-136">值</span><span class="sxs-lookup"><span data-stu-id="aba1a-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba1a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aba1a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="aba1a-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aba1a-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aba1a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aba1a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="aba1a-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aba1a-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aba1a-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="aba1a-141">Namespace</span></span><br/>                | <span data-ttu-id="aba1a-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="aba1a-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aba1a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="aba1a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aba1a-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="aba1a-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aba1a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="aba1a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aba1a-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aba1a-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

