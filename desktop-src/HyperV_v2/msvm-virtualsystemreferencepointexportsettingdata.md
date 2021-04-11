---
description: 提供要與 Msvm VirtualSystemReferencePointService 類別的 ExportReferencePoint 方法搭配使用的其他資訊 \_ 。
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Msvm_VirtualSystemReferencePointExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027668"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="cb4ed-103">Msvm \_ VirtualSystemReferencePointExportSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="cb4ed-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="cb4ed-104">提供要與 [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)類別的 [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)方法搭配使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="cb4ed-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="cb4ed-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb4ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4ed-106">語法</span><span class="sxs-lookup"><span data-stu-id="cb4ed-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="cb4ed-107">成員</span><span class="sxs-lookup"><span data-stu-id="cb4ed-107">Members</span></span>

<span data-ttu-id="cb4ed-108">**Msvm \_ VirtualSystemReferencePointExportSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cb4ed-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cb4ed-109">屬性</span><span class="sxs-lookup"><span data-stu-id="cb4ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb4ed-110">屬性</span><span class="sxs-lookup"><span data-stu-id="cb4ed-110">Properties</span></span>

<span data-ttu-id="cb4ed-111">**Msvm \_ VirtualSystemReferencePointExportSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cb4ed-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb4ed-112">**BaseReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="cb4ed-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb4ed-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cb4ed-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="cb4ed-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb4ed-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb4ed-115">應該執行匯出之基底參考點的路徑。</span><span class="sxs-lookup"><span data-stu-id="cb4ed-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="cb4ed-116">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="cb4ed-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb4ed-117">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="cb4ed-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="cb4ed-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb4ed-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb4ed-119">需要匯出資料之磁片的 WMI 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb4ed-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb4ed-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb4ed-120">Requirements</span></span>



| <span data-ttu-id="cb4ed-121">需求</span><span class="sxs-lookup"><span data-stu-id="cb4ed-121">Requirement</span></span> | <span data-ttu-id="cb4ed-122">值</span><span class="sxs-lookup"><span data-stu-id="cb4ed-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4ed-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb4ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4ed-124">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb4ed-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cb4ed-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb4ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4ed-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb4ed-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cb4ed-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb4ed-127">Namespace</span></span><br/>                | <span data-ttu-id="cb4ed-128">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb4ed-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb4ed-129">MOF</span><span class="sxs-lookup"><span data-stu-id="cb4ed-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb4ed-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cb4ed-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb4ed-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cb4ed-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb4ed-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb4ed-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb4ed-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb4ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb4ed-134">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="cb4ed-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




