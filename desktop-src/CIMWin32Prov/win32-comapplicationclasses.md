---
description: Win32 \_ COMApplicationClasses 抽象關聯 WMI 類別會將元件物件模型與 com) 元件以及它所在的 com 應用程式 (相關聯。
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Win32_COMApplicationClasses 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111232"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="65dbd-103">Win32 \_ COMApplicationClasses 類別</span><span class="sxs-lookup"><span data-stu-id="65dbd-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="65dbd-104">**Win32 \_ COMApplicationClasses** 抽象關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將元件物件模型與 com) 元件以及它所在的 com 應用程式 (相關聯。</span><span class="sxs-lookup"><span data-stu-id="65dbd-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="65dbd-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="65dbd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="65dbd-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="65dbd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65dbd-107">語法</span><span class="sxs-lookup"><span data-stu-id="65dbd-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="65dbd-108">成員</span><span class="sxs-lookup"><span data-stu-id="65dbd-108">Members</span></span>

<span data-ttu-id="65dbd-109">**Win32 \_ COMApplicationClasses** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65dbd-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="65dbd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="65dbd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65dbd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="65dbd-111">Properties</span></span>

<span data-ttu-id="65dbd-112">**Win32 \_ COMApplicationClasses** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65dbd-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65dbd-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="65dbd-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dbd-114">資料類型： **Win32 \_ COMApplication**</span><span class="sxs-lookup"><span data-stu-id="65dbd-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="65dbd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65dbd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dbd-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ COMApplication" ) </span><span class="sxs-lookup"><span data-stu-id="65dbd-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="65dbd-117">[**Win32 \_ COMApplication**](win32-comapplication.md) ，表示包含 COM 元件的 com 應用程式。</span><span class="sxs-lookup"><span data-stu-id="65dbd-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="65dbd-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="65dbd-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65dbd-119">資料類型： **Win32 \_ comclass.zip**</span><span class="sxs-lookup"><span data-stu-id="65dbd-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="65dbd-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65dbd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65dbd-121">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ comclass.zip" ) </span><span class="sxs-lookup"><span data-stu-id="65dbd-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="65dbd-122">[**Win32 \_ comclass.zip**](win32-comclass.md) ，代表在 com 應用程式底下分組的 com 元件。</span><span class="sxs-lookup"><span data-stu-id="65dbd-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65dbd-123">備註</span><span class="sxs-lookup"><span data-stu-id="65dbd-123">Remarks</span></span>

<span data-ttu-id="65dbd-124">**Win32 \_ COMApplicationClasses** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="65dbd-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65dbd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="65dbd-125">Requirements</span></span>



| <span data-ttu-id="65dbd-126">需求</span><span class="sxs-lookup"><span data-stu-id="65dbd-126">Requirement</span></span> | <span data-ttu-id="65dbd-127">值</span><span class="sxs-lookup"><span data-stu-id="65dbd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65dbd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65dbd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="65dbd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65dbd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65dbd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65dbd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="65dbd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65dbd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65dbd-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="65dbd-132">Namespace</span></span><br/>                | <span data-ttu-id="65dbd-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65dbd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65dbd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="65dbd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65dbd-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="65dbd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65dbd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="65dbd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65dbd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65dbd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65dbd-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65dbd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65dbd-139">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="65dbd-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="65dbd-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65dbd-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

