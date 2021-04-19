---
description: 將設定資料匯出為傳入 Msvm CollectionReferencePointService 類別的 ExportReferencePoint 方法 \_ 。
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985068"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="97c73-103">Msvm \_ CollectionReferencePointExportSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="97c73-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="97c73-104">將設定資料匯出為傳入 [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)類別的 [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)方法。</span><span class="sxs-lookup"><span data-stu-id="97c73-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="97c73-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="97c73-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c73-106">語法</span><span class="sxs-lookup"><span data-stu-id="97c73-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="97c73-107">成員</span><span class="sxs-lookup"><span data-stu-id="97c73-107">Members</span></span>

<span data-ttu-id="97c73-108">**Msvm \_ CollectionReferencePointExportSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97c73-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="97c73-109">屬性</span><span class="sxs-lookup"><span data-stu-id="97c73-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97c73-110">屬性</span><span class="sxs-lookup"><span data-stu-id="97c73-110">Properties</span></span>

<span data-ttu-id="97c73-111">**Msvm \_ CollectionReferencePointExportSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="97c73-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97c73-112">**BaseReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="97c73-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97c73-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="97c73-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97c73-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="97c73-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="97c73-115">[**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)實例的路徑，代表要用於差異匯出的基底參考點集合。</span><span class="sxs-lookup"><span data-stu-id="97c73-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="97c73-116">**VirtualMachinesToDisksToExport**</span><span class="sxs-lookup"><span data-stu-id="97c73-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97c73-117">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="97c73-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="97c73-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="97c73-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97c73-119">限定詞： **HyperVEmbeddedInstance** ( "Msvm \_ VirtualMachineToDisks" ) </span><span class="sxs-lookup"><span data-stu-id="97c73-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="97c73-120">需要匯出資料的「VirtualMachines 至 DisksToExport」對應資訊的清單。</span><span class="sxs-lookup"><span data-stu-id="97c73-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97c73-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="97c73-121">Requirements</span></span>



| <span data-ttu-id="97c73-122">需求</span><span class="sxs-lookup"><span data-stu-id="97c73-122">Requirement</span></span> | <span data-ttu-id="97c73-123">值</span><span class="sxs-lookup"><span data-stu-id="97c73-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c73-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97c73-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97c73-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97c73-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="97c73-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97c73-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97c73-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="97c73-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="97c73-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="97c73-128">Namespace</span></span><br/>                | <span data-ttu-id="97c73-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="97c73-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="97c73-130">MOF</span><span class="sxs-lookup"><span data-stu-id="97c73-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97c73-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="97c73-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97c73-132">DLL</span><span class="sxs-lookup"><span data-stu-id="97c73-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97c73-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97c73-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97c73-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97c73-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c73-135">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="97c73-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




