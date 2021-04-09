---
description: 代表可讓使用者輸入、查看或聆聽電腦系統上資料的邏輯裝置。
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: 'CIM_UserDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848787"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="18d7b-103">CIM_UserDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="18d7b-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="18d7b-104">代表可讓使用者輸入、查看或聆聽電腦系統上資料的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="18d7b-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="18d7b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="18d7b-106">成員</span><span class="sxs-lookup"><span data-stu-id="18d7b-106">Members</span></span>

<span data-ttu-id="18d7b-107">**CIM \_ UserDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18d7b-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="18d7b-108">屬性</span><span class="sxs-lookup"><span data-stu-id="18d7b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18d7b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="18d7b-109">Properties</span></span>

<span data-ttu-id="18d7b-110">**CIM \_ UserDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18d7b-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18d7b-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="18d7b-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d7b-112">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18d7b-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d7b-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18d7b-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d7b-114">如果裝置已鎖定，防止使用者輸入或輸出，則 **為 true** 。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="18d7b-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18d7b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="18d7b-115">Requirements</span></span>



| <span data-ttu-id="18d7b-116">需求</span><span class="sxs-lookup"><span data-stu-id="18d7b-116">Requirement</span></span> | <span data-ttu-id="18d7b-117">值</span><span class="sxs-lookup"><span data-stu-id="18d7b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d7b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18d7b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18d7b-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="18d7b-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="18d7b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18d7b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18d7b-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18d7b-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="18d7b-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="18d7b-122">Namespace</span></span><br/>                | <span data-ttu-id="18d7b-123">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="18d7b-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18d7b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="18d7b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18d7b-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18d7b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="18d7b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d7b-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18d7b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18d7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d7b-129">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="18d7b-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




