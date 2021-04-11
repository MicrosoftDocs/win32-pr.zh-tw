---
description: Win32 \_ ClassicCOMApplicationClasses 關聯 WMI 類別會關聯 com 應用程式和其下分組的 com 元件。
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Win32_ClassicCOMApplicationClasses 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847491"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="84cfb-103">Win32 \_ ClassicCOMApplicationClasses 類別</span><span class="sxs-lookup"><span data-stu-id="84cfb-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="84cfb-104">**Win32 \_ ClassicCOMApplicationClasses** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯 com 應用程式和其下分組的 com 元件。</span><span class="sxs-lookup"><span data-stu-id="84cfb-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="84cfb-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="84cfb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="84cfb-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="84cfb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84cfb-107">語法</span><span class="sxs-lookup"><span data-stu-id="84cfb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="84cfb-108">成員</span><span class="sxs-lookup"><span data-stu-id="84cfb-108">Members</span></span>

<span data-ttu-id="84cfb-109">**Win32 \_ ClassicCOMApplicationClasses** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84cfb-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="84cfb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84cfb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84cfb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="84cfb-111">Properties</span></span>

<span data-ttu-id="84cfb-112">**Win32 \_ ClassicCOMApplicationClasses** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84cfb-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84cfb-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="84cfb-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cfb-114">資料類型： **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="84cfb-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="84cfb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84cfb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84cfb-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DCOMApplication" ) </span><span class="sxs-lookup"><span data-stu-id="84cfb-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="84cfb-117">[**Win32 \_ DCOMApplication**](win32-dcomapplication.md) ，代表包含或使用 COM 元件的 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="84cfb-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="84cfb-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="84cfb-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cfb-119">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="84cfb-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="84cfb-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84cfb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84cfb-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="84cfb-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="84cfb-122">[**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md) ，表示 DCOM 應用程式中現有的 COM 元件或使用的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="84cfb-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84cfb-123">備註</span><span class="sxs-lookup"><span data-stu-id="84cfb-123">Remarks</span></span>

<span data-ttu-id="84cfb-124">**Win32 \_ ClassicCOMApplicationClasses** 類別衍生自 [**win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md)。</span><span class="sxs-lookup"><span data-stu-id="84cfb-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84cfb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="84cfb-125">Requirements</span></span>



| <span data-ttu-id="84cfb-126">需求</span><span class="sxs-lookup"><span data-stu-id="84cfb-126">Requirement</span></span> | <span data-ttu-id="84cfb-127">值</span><span class="sxs-lookup"><span data-stu-id="84cfb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84cfb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84cfb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="84cfb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84cfb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84cfb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84cfb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="84cfb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84cfb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84cfb-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="84cfb-132">Namespace</span></span><br/>                | <span data-ttu-id="84cfb-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84cfb-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84cfb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="84cfb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84cfb-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="84cfb-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84cfb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="84cfb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84cfb-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84cfb-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84cfb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84cfb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cfb-139">**Win32 \_ COMApplicationClasses**</span><span class="sxs-lookup"><span data-stu-id="84cfb-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="84cfb-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84cfb-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

