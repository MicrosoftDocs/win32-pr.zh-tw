---
description: Win32 \_ DependentService 關聯 WMI 類別會關聯兩個相互依存的基礎服務。
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Win32_DependentService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111608"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="6c3d8-103">Win32 \_ DependentService 類別</span><span class="sxs-lookup"><span data-stu-id="6c3d8-103">Win32\_DependentService class</span></span>

<span data-ttu-id="6c3d8-104">**Win32 \_ DependentService** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯兩個相互依存的基礎服務。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="6c3d8-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6c3d8-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c3d8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6c3d8-108">成員</span><span class="sxs-lookup"><span data-stu-id="6c3d8-108">Members</span></span>

<span data-ttu-id="6c3d8-109">**Win32 \_ DependentService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c3d8-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="6c3d8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6c3d8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c3d8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6c3d8-111">Properties</span></span>

<span data-ttu-id="6c3d8-112">**Win32 \_ DependentService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c3d8-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3d8-114">資料類型： **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="6c3d8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c3d8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c3d8-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ BaseService" ) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="6c3d8-117">代表基底服務的 [**Win32 \_ BaseService**](win32-baseservice.md) 依賴這個類別的 **相依** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="6c3d8-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3d8-119">資料類型： **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="6c3d8-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c3d8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c3d8-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 BaseService」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="6c3d8-122">[**Win32 \_ BaseService**](win32-baseservice.md) ，代表相依于這個類別之 **Antecedent** 屬性的基底服務。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="6c3d8-123">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3d8-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c3d8-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c3d8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3d8-126">服務對服務相依性的本質。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="6c3d8-127">這個屬性工作表示相關聯的服務必須已完成、必須啟動，或不能啟動，服務才能運作。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="6c3d8-128">這個屬性繼承自 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c3d8-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c3d8-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="6c3d8-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**服務必須已完成** (2) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c3d8-132">服務必須已完成。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="6c3d8-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**服務必須啟動** (3) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c3d8-134">必須啟動服務。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="6c3d8-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**服務不得啟動** (4) </span><span class="sxs-lookup"><span data-stu-id="6c3d8-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6c3d8-136">服務不得啟動。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c3d8-137">備註</span><span class="sxs-lookup"><span data-stu-id="6c3d8-137">Remarks</span></span>

<span data-ttu-id="6c3d8-138">**Win32 \_ DependentService** 類別衍生自 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3d8-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3d8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c3d8-139">Requirements</span></span>



| <span data-ttu-id="6c3d8-140">需求</span><span class="sxs-lookup"><span data-stu-id="6c3d8-140">Requirement</span></span> | <span data-ttu-id="6c3d8-141">值</span><span class="sxs-lookup"><span data-stu-id="6c3d8-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3d8-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c3d8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3d8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c3d8-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c3d8-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c3d8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3d8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c3d8-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c3d8-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c3d8-146">Namespace</span></span><br/>                | <span data-ttu-id="6c3d8-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c3d8-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c3d8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6c3d8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c3d8-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d8-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c3d8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6c3d8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c3d8-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d8-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c3d8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c3d8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3d8-153">**CIM \_ ServiceServiceDependency**</span><span class="sxs-lookup"><span data-stu-id="6c3d8-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="6c3d8-154">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c3d8-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

