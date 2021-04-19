---
description: 表示度量服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 ModifyServiceSettings 方法來修改任何這些屬性。
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Msvm_MetricServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980772"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="d3bb5-105">Msvm \_ MetricServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="d3bb5-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="d3bb5-106">表示度量服務的設定。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="d3bb5-107">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="d3bb5-108">用戶端必須呼叫 [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) 方法來修改任何這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="d3bb5-109">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3bb5-110">語法</span><span class="sxs-lookup"><span data-stu-id="d3bb5-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="d3bb5-111">成員</span><span class="sxs-lookup"><span data-stu-id="d3bb5-111">Members</span></span>

<span data-ttu-id="d3bb5-112">**Msvm \_ MetricServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3bb5-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d3bb5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d3bb5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3bb5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d3bb5-114">Properties</span></span>

<span data-ttu-id="d3bb5-115">**Msvm \_ MetricServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3bb5-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3bb5-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3bb5-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3bb5-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-119">A short description of the object.</span></span> <span data-ttu-id="d3bb5-120">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務設定」。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d3bb5-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3bb5-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3bb5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3bb5-124">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-124">A description of the object.</span></span> <span data-ttu-id="d3bb5-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「定義 Hyper-v 計量服務設定」。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d3bb5-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3bb5-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3bb5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3bb5-129">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-129">A display name for the object.</span></span> <span data-ttu-id="d3bb5-130">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務設定」。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d3bb5-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3bb5-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3bb5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-134">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d3bb5-135">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d3bb5-136">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d3bb5-137">**MetricsFlushInterval**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3bb5-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d3bb5-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3bb5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3bb5-140">定義應將計量排清至磁片的間隔。</span><span class="sxs-lookup"><span data-stu-id="d3bb5-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3bb5-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3bb5-141">Requirements</span></span>



| <span data-ttu-id="d3bb5-142">需求</span><span class="sxs-lookup"><span data-stu-id="d3bb5-142">Requirement</span></span> | <span data-ttu-id="d3bb5-143">值</span><span class="sxs-lookup"><span data-stu-id="d3bb5-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3bb5-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3bb5-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d3bb5-145">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3bb5-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3bb5-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3bb5-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d3bb5-147">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3bb5-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3bb5-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3bb5-148">Namespace</span></span><br/>                | <span data-ttu-id="d3bb5-149">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d3bb5-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3bb5-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d3bb5-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3bb5-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d3bb5-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3bb5-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d3bb5-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3bb5-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3bb5-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3bb5-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3bb5-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3bb5-155">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="d3bb5-156">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="d3bb5-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

