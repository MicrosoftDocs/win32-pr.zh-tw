---
description: 表示必須透過媒體存取裝置存取儲存區的關聯性。
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: 'CIM_MediaPresent 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997313"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="bf484-103">CIM_MediaPresent 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="bf484-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="bf484-104">表示必須透過媒體存取裝置存取儲存區的關聯性。</span><span class="sxs-lookup"><span data-stu-id="bf484-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf484-105">語法</span><span class="sxs-lookup"><span data-stu-id="bf484-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="bf484-106">成員</span><span class="sxs-lookup"><span data-stu-id="bf484-106">Members</span></span>

<span data-ttu-id="bf484-107">**CIM \_ MediaPresent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf484-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="bf484-108">屬性</span><span class="sxs-lookup"><span data-stu-id="bf484-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf484-109">屬性</span><span class="sxs-lookup"><span data-stu-id="bf484-109">Properties</span></span>

<span data-ttu-id="bf484-110">**CIM \_ MediaPresent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf484-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf484-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="bf484-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf484-112">資料類型： **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="bf484-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bf484-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf484-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf484-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="bf484-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bf484-115">媒體存取裝置。</span><span class="sxs-lookup"><span data-stu-id="bf484-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="bf484-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="bf484-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf484-117">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="bf484-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="bf484-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf484-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf484-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="bf484-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bf484-120">使用媒體存取裝置時所存取的儲存區。</span><span class="sxs-lookup"><span data-stu-id="bf484-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="bf484-121">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="bf484-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf484-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bf484-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf484-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bf484-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf484-124">如果媒體存取裝置中的儲存區已固定且無法取出，則 **為 true** 。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="bf484-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf484-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf484-125">Requirements</span></span>



| <span data-ttu-id="bf484-126">需求</span><span class="sxs-lookup"><span data-stu-id="bf484-126">Requirement</span></span> | <span data-ttu-id="bf484-127">值</span><span class="sxs-lookup"><span data-stu-id="bf484-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf484-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf484-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bf484-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bf484-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bf484-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf484-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bf484-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf484-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bf484-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf484-132">Namespace</span></span><br/>                | <span data-ttu-id="bf484-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="bf484-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf484-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bf484-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf484-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bf484-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf484-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bf484-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf484-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf484-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf484-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf484-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf484-139">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="bf484-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

