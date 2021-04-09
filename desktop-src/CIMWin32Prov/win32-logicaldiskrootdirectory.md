---
description: Win32 \_ LogicalDiskRootDirectory 關聯 WMI 類別會建立邏輯磁片與其目錄結構的關聯。
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Win32_LogicalDiskRootDirectory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847040"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="b14b8-103">Win32 \_ LogicalDiskRootDirectory 類別</span><span class="sxs-lookup"><span data-stu-id="b14b8-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="b14b8-104">**Win32 \_ LogicalDiskRootDirectory** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立邏輯磁片與其目錄結構的關聯。</span><span class="sxs-lookup"><span data-stu-id="b14b8-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="b14b8-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b14b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b14b8-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b14b8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="b14b8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b14b8-108">成員</span><span class="sxs-lookup"><span data-stu-id="b14b8-108">Members</span></span>

<span data-ttu-id="b14b8-109">**Win32 \_ LogicalDiskRootDirectory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b14b8-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="b14b8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b14b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b14b8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b14b8-111">Properties</span></span>

<span data-ttu-id="b14b8-112">**Win32 \_ LogicalDiskRootDirectory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b14b8-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b14b8-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b14b8-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14b8-114">資料類型： **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="b14b8-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="b14b8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b14b8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14b8-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LogicalDisk" ) </span><span class="sxs-lookup"><span data-stu-id="b14b8-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="b14b8-117">代表邏輯磁片屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b14b8-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="b14b8-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b14b8-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14b8-119">資料類型： **Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="b14b8-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="b14b8-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b14b8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14b8-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ Directory" ) </span><span class="sxs-lookup"><span data-stu-id="b14b8-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="b14b8-122">代表檔案目錄結構屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b14b8-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b14b8-123">備註</span><span class="sxs-lookup"><span data-stu-id="b14b8-123">Remarks</span></span>

<span data-ttu-id="b14b8-124">**Win32 \_ LogicalDiskRootDirectory** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="b14b8-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b14b8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b14b8-125">Requirements</span></span>



| <span data-ttu-id="b14b8-126">需求</span><span class="sxs-lookup"><span data-stu-id="b14b8-126">Requirement</span></span> | <span data-ttu-id="b14b8-127">值</span><span class="sxs-lookup"><span data-stu-id="b14b8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b14b8-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b14b8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b14b8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b14b8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b14b8-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b14b8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b14b8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b14b8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b14b8-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b14b8-132">Namespace</span></span><br/>                | <span data-ttu-id="b14b8-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b14b8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b14b8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b14b8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b14b8-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b14b8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b14b8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b14b8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b14b8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b14b8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14b8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b14b8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14b8-139">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="b14b8-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="b14b8-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b14b8-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

