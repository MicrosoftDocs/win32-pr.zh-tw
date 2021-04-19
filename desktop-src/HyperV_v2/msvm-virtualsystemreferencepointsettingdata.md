---
description: 提供要與 Msvm VirtualSystemReferencePointService 類別的 CreateReferencePoint 方法搭配使用的其他資訊 \_ 。
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Msvm_VirtualSystemReferencePointSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993779"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="ee20d-103">Msvm \_ VirtualSystemReferencePointSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="ee20d-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="ee20d-104">提供要與 [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)類別的 [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)方法搭配使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ee20d-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="ee20d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ee20d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee20d-106">語法</span><span class="sxs-lookup"><span data-stu-id="ee20d-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="ee20d-107">成員</span><span class="sxs-lookup"><span data-stu-id="ee20d-107">Members</span></span>

<span data-ttu-id="ee20d-108">**Msvm \_ VirtualSystemReferencePointSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ee20d-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ee20d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ee20d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee20d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ee20d-110">Properties</span></span>

<span data-ttu-id="ee20d-111">**Msvm \_ VirtualSystemReferencePointSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ee20d-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee20d-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="ee20d-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee20d-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="ee20d-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ee20d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee20d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee20d-115">參考點的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="ee20d-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee20d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee20d-116">Requirements</span></span>



| <span data-ttu-id="ee20d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ee20d-117">Requirement</span></span> | <span data-ttu-id="ee20d-118">值</span><span class="sxs-lookup"><span data-stu-id="ee20d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee20d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee20d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee20d-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee20d-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ee20d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee20d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee20d-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ee20d-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ee20d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="ee20d-123">Namespace</span></span><br/>                | <span data-ttu-id="ee20d-124">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ee20d-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ee20d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ee20d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee20d-126"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ee20d-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee20d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee20d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee20d-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee20d-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee20d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee20d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee20d-130">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="ee20d-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




