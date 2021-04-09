---
description: 將資料設定為以陣列形式傳遞至 Msvm \_ CollectionReferencePointExportSettingData 類別。
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Msvm_VirtualMachineToDisks 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847765"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="223d9-103">Msvm \_ VirtualMachineToDisks 類別</span><span class="sxs-lookup"><span data-stu-id="223d9-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="223d9-104">將資料設定為以陣列形式傳遞至 [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="223d9-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="223d9-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="223d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="223d9-106">語法</span><span class="sxs-lookup"><span data-stu-id="223d9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="223d9-107">成員</span><span class="sxs-lookup"><span data-stu-id="223d9-107">Members</span></span>

<span data-ttu-id="223d9-108">**Msvm \_ VirtualMachineToDisks** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="223d9-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="223d9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="223d9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="223d9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="223d9-110">Properties</span></span>

<span data-ttu-id="223d9-111">**Msvm \_ VirtualMachineToDisks** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="223d9-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="223d9-112">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="223d9-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="223d9-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="223d9-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="223d9-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="223d9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="223d9-115">需要匯出資料之特定虛擬機器識別碼所屬磁片的 WMI 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="223d9-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="223d9-116">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="223d9-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="223d9-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="223d9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="223d9-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="223d9-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="223d9-119">與虛擬磁片相關聯的虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="223d9-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="223d9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="223d9-120">Requirements</span></span>



| <span data-ttu-id="223d9-121">需求</span><span class="sxs-lookup"><span data-stu-id="223d9-121">Requirement</span></span> | <span data-ttu-id="223d9-122">值</span><span class="sxs-lookup"><span data-stu-id="223d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="223d9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="223d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="223d9-124">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="223d9-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="223d9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="223d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="223d9-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="223d9-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="223d9-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="223d9-127">Namespace</span></span><br/>                | <span data-ttu-id="223d9-128">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="223d9-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="223d9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="223d9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="223d9-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="223d9-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="223d9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="223d9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="223d9-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="223d9-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




