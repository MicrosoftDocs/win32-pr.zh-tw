---
description: 代表存在於單一主機系統上的綜合3-d 服務的設定。
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Msvm_Synthetic3DServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114957"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="5bd2e-103">Msvm \_ Synthetic3DServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="5bd2e-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="5bd2e-104">代表存在於單一主機系統上的綜合3-d 服務的設定。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="5bd2e-105">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="5bd2e-106">用戶端必須呼叫 [**Msvm \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) 方法來修改任何這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="5bd2e-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="5bd2e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="5bd2e-109">成員</span><span class="sxs-lookup"><span data-stu-id="5bd2e-109">Members</span></span>

<span data-ttu-id="5bd2e-110">**Msvm \_ Synthetic3DServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5bd2e-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5bd2e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5bd2e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bd2e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5bd2e-112">Properties</span></span>

<span data-ttu-id="5bd2e-113">**Msvm \_ Synthetic3DServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bd2e-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd2e-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd2e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd2e-117">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-117">A short description of the object.</span></span> <span data-ttu-id="5bd2e-118">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5bd2e-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd2e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd2e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd2e-122">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-122">A description of the object.</span></span> <span data-ttu-id="5bd2e-123">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5bd2e-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd2e-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd2e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd2e-127">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-127">A display name for the object.</span></span> <span data-ttu-id="5bd2e-128">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5bd2e-129">**GPUOvercommitEnabled**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd2e-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd2e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd2e-132">控制虛擬機器指派是否會將 GPU 記憶體限制納入考慮。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="5bd2e-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd2e-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd2e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd2e-136">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5bd2e-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5bd2e-137">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5bd2e-138">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5bd2e-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5bd2e-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bd2e-139">Requirements</span></span>



| <span data-ttu-id="5bd2e-140">需求</span><span class="sxs-lookup"><span data-stu-id="5bd2e-140">Requirement</span></span> | <span data-ttu-id="5bd2e-141">值</span><span class="sxs-lookup"><span data-stu-id="5bd2e-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd2e-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bd2e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd2e-143">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bd2e-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5bd2e-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bd2e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd2e-145">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bd2e-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5bd2e-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="5bd2e-146">Namespace</span></span><br/>                | <span data-ttu-id="5bd2e-147">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5bd2e-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5bd2e-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5bd2e-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bd2e-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5bd2e-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bd2e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd2e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd2e-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bd2e-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

