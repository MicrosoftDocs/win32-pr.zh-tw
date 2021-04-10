---
description: CIM \_ MediaPresent 關聯描述必須透過媒體存取裝置存取儲存區的關聯性。
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: 'CIM_MediaPresent 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853424"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="a769d-103">CIM_MediaPresent 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="a769d-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a769d-104">**CIM \_ MediaPresent** 關聯描述必須透過媒體存取裝置存取儲存區的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a769d-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a769d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a769d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a769d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a769d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a769d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a769d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a769d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a769d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a769d-109">語法</span><span class="sxs-lookup"><span data-stu-id="a769d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a769d-110">成員</span><span class="sxs-lookup"><span data-stu-id="a769d-110">Members</span></span>

<span data-ttu-id="a769d-111">**CIM \_ MediaPresent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a769d-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="a769d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a769d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a769d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a769d-113">Properties</span></span>

<span data-ttu-id="a769d-114">**CIM \_ MediaPresent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a769d-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a769d-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="a769d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a769d-116">資料類型： **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="a769d-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a769d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a769d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a769d-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="a769d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a769d-119">描述媒體存取裝置的 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="a769d-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="a769d-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="a769d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a769d-121">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="a769d-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="a769d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a769d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a769d-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="a769d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a769d-124">[**CIM \_ StorageExtent**](cim-storageextent.md) ，描述使用媒體存取裝置所存取的儲存區。</span><span class="sxs-lookup"><span data-stu-id="a769d-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a769d-125">備註</span><span class="sxs-lookup"><span data-stu-id="a769d-125">Remarks</span></span>

<span data-ttu-id="a769d-126">**Cim \_ MediaPresent** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="a769d-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a769d-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a769d-127">WMI does not implement this class.</span></span> <span data-ttu-id="a769d-128">針對衍生自 **CIM \_ MediaPresent** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a769d-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a769d-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a769d-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a769d-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a769d-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a769d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a769d-131">Requirements</span></span>



| <span data-ttu-id="a769d-132">需求</span><span class="sxs-lookup"><span data-stu-id="a769d-132">Requirement</span></span> | <span data-ttu-id="a769d-133">值</span><span class="sxs-lookup"><span data-stu-id="a769d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a769d-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a769d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a769d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a769d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a769d-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a769d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a769d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a769d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a769d-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="a769d-138">Namespace</span></span><br/>                | <span data-ttu-id="a769d-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a769d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a769d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a769d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a769d-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a769d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a769d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a769d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a769d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a769d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a769d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a769d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a769d-145">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="a769d-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

