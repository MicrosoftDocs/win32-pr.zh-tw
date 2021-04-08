---
description: 將存放磁片磁碟機與插入磁片磁碟機的媒體產生關聯。
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853476"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="6f140-103">Msvm \_ MediaPresent 類別</span><span class="sxs-lookup"><span data-stu-id="6f140-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="6f140-104">將存放磁片磁碟機與插入磁片磁碟機的媒體產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6f140-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="6f140-105">此關聯用於所有存放磁片磁碟機物件。</span><span class="sxs-lookup"><span data-stu-id="6f140-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="6f140-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f140-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f140-107">語法</span><span class="sxs-lookup"><span data-stu-id="6f140-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="6f140-108">成員</span><span class="sxs-lookup"><span data-stu-id="6f140-108">Members</span></span>

<span data-ttu-id="6f140-109">**Msvm \_ MediaPresent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f140-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="6f140-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6f140-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f140-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6f140-111">Properties</span></span>

<span data-ttu-id="6f140-112">**Msvm \_ MediaPresent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f140-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f140-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="6f140-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f140-114">資料類型： **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="6f140-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="6f140-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f140-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f140-116">媒體存取裝置的參考。</span><span class="sxs-lookup"><span data-stu-id="6f140-116">The reference to the media access device.</span></span> <span data-ttu-id="6f140-117">這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。</span><span class="sxs-lookup"><span data-stu-id="6f140-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="6f140-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6f140-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f140-119">資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="6f140-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="6f140-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f140-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f140-121">使用媒體存取裝置存取的儲存範圍參考。</span><span class="sxs-lookup"><span data-stu-id="6f140-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="6f140-122">這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。</span><span class="sxs-lookup"><span data-stu-id="6f140-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="6f140-123">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="6f140-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f140-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f140-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f140-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f140-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f140-126">指出存取的儲存區是否為固定的，且無法被退出。</span><span class="sxs-lookup"><span data-stu-id="6f140-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="6f140-127">硬碟的值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="6f140-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="6f140-128">這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。</span><span class="sxs-lookup"><span data-stu-id="6f140-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f140-129">備註</span><span class="sxs-lookup"><span data-stu-id="6f140-129">Remarks</span></span>

<span data-ttu-id="6f140-130">存取 **Msvm \_ MediaPresent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="6f140-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6f140-131">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="6f140-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f140-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f140-132">Requirements</span></span>



| <span data-ttu-id="6f140-133">需求</span><span class="sxs-lookup"><span data-stu-id="6f140-133">Requirement</span></span> | <span data-ttu-id="6f140-134">值</span><span class="sxs-lookup"><span data-stu-id="6f140-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f140-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f140-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f140-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f140-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f140-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f140-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f140-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f140-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f140-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f140-139">Namespace</span></span><br/>                | <span data-ttu-id="6f140-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f140-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f140-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6f140-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f140-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6f140-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f140-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6f140-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f140-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f140-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f140-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f140-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f140-146">**CIM \_ MediaPresent**</span><span class="sxs-lookup"><span data-stu-id="6f140-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="6f140-147">**CIM \_ MediaPresent**</span><span class="sxs-lookup"><span data-stu-id="6f140-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="6f140-148">儲存類別</span><span class="sxs-lookup"><span data-stu-id="6f140-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

