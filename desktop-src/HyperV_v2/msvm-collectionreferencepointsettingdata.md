---
description: 提供要與 Msvm CollectionReferencePointService 類別的 CreateReferencePoint 方法搭配使用的其他資訊 \_ 。
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Msvm_CollectionReferencePointSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114581"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="9b561-103">Msvm \_ CollectionReferencePointSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="9b561-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="9b561-104">提供要與 [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)類別的 [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md)方法搭配使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="9b561-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="9b561-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b561-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b561-106">語法</span><span class="sxs-lookup"><span data-stu-id="9b561-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="9b561-107">成員</span><span class="sxs-lookup"><span data-stu-id="9b561-107">Members</span></span>

<span data-ttu-id="9b561-108">**Msvm \_ CollectionReferencePointSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9b561-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9b561-109">屬性</span><span class="sxs-lookup"><span data-stu-id="9b561-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b561-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9b561-110">Properties</span></span>

<span data-ttu-id="9b561-111">**Msvm \_ CollectionReferencePointSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9b561-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b561-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="9b561-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b561-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9b561-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b561-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9b561-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b561-115">參考點的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="9b561-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b561-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9b561-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="9b561-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**應用程式一致** (1) </span><span class="sxs-lookup"><span data-stu-id="9b561-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9b561-118">參考點表示虛擬系統處於損毀一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="9b561-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="9b561-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>損 **毀一致** (2) </span><span class="sxs-lookup"><span data-stu-id="9b561-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b561-120">參考點表示虛擬系統處於應用程式一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="9b561-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b561-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b561-121">Requirements</span></span>



| <span data-ttu-id="9b561-122">需求</span><span class="sxs-lookup"><span data-stu-id="9b561-122">Requirement</span></span> | <span data-ttu-id="9b561-123">值</span><span class="sxs-lookup"><span data-stu-id="9b561-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b561-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b561-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b561-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b561-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9b561-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b561-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b561-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9b561-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9b561-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="9b561-128">Namespace</span></span><br/>                | <span data-ttu-id="9b561-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9b561-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9b561-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9b561-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b561-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9b561-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b561-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b561-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b561-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b561-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b561-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b561-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b561-135">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="9b561-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




