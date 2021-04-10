---
description: 將虛擬硬碟從來源移到目的地路徑。
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Msvm_MoveUnmanagedVhd 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852383"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="16173-103">Msvm \_ MoveUnmanagedVhd 類別</span><span class="sxs-lookup"><span data-stu-id="16173-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="16173-104">將虛擬硬碟從來源移到目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="16173-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="16173-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16173-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16173-106">語法</span><span class="sxs-lookup"><span data-stu-id="16173-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="16173-107">成員</span><span class="sxs-lookup"><span data-stu-id="16173-107">Members</span></span>

<span data-ttu-id="16173-108">**Msvm \_ MoveUnmanagedVhd** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16173-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="16173-109">屬性</span><span class="sxs-lookup"><span data-stu-id="16173-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16173-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16173-110">Properties</span></span>

<span data-ttu-id="16173-111">**Msvm \_ MoveUnmanagedVhd** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16173-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16173-112">**VhdDestinationPath**</span><span class="sxs-lookup"><span data-stu-id="16173-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16173-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16173-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16173-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16173-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16173-115">目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="16173-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="16173-116">**VhdSourcePath**</span><span class="sxs-lookup"><span data-stu-id="16173-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16173-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="16173-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16173-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16173-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16173-119">要移動之虛擬硬碟的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="16173-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16173-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="16173-120">Requirements</span></span>



| <span data-ttu-id="16173-121">需求</span><span class="sxs-lookup"><span data-stu-id="16173-121">Requirement</span></span> | <span data-ttu-id="16173-122">值</span><span class="sxs-lookup"><span data-stu-id="16173-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16173-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16173-123">Minimum supported client</span></span><br/> | <span data-ttu-id="16173-124">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16173-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="16173-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16173-125">Minimum supported server</span></span><br/> | <span data-ttu-id="16173-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="16173-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="16173-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="16173-127">Namespace</span></span><br/>                | <span data-ttu-id="16173-128">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="16173-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16173-129">MOF</span><span class="sxs-lookup"><span data-stu-id="16173-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16173-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16173-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16173-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16173-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16173-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16173-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16173-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16173-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16173-134">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16173-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




