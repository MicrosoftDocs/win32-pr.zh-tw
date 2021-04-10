---
description: Win32 \_ ImplementedCategory 關聯 WMI 類別使用其介面 (COM) 類別的元件類別和元件物件模型相關聯。
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Win32_ImplementedCategory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689184"
---
# <a name="win32_implementedcategory-class"></a><span data-ttu-id="ae12b-103">Win32 \_ ImplementedCategory 類別</span><span class="sxs-lookup"><span data-stu-id="ae12b-103">Win32\_ImplementedCategory class</span></span>

<span data-ttu-id="ae12b-104">**Win32 \_ ImplementedCategory** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)使用其介面 (COM) 類別的元件類別和元件物件模型相關聯。</span><span class="sxs-lookup"><span data-stu-id="ae12b-104">The **Win32\_ImplementedCategory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a component category and the Component Object Model (COM) class using its interfaces.</span></span>

<span data-ttu-id="ae12b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae12b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae12b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ae12b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae12b-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae12b-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a><span data-ttu-id="ae12b-108">成員</span><span class="sxs-lookup"><span data-stu-id="ae12b-108">Members</span></span>

<span data-ttu-id="ae12b-109">**Win32 \_ ImplementedCategory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ae12b-109">The **Win32\_ImplementedCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="ae12b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ae12b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae12b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ae12b-111">Properties</span></span>

<span data-ttu-id="ae12b-112">**Win32 \_ ImplementedCategory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ae12b-112">The **Win32\_ImplementedCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae12b-113">**類別**</span><span class="sxs-lookup"><span data-stu-id="ae12b-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae12b-114">資料類型： **Win32 \_ ComponentCategory**</span><span class="sxs-lookup"><span data-stu-id="ae12b-114">Data type: **Win32\_ComponentCategory**</span></span>
</dt> <dt>

<span data-ttu-id="ae12b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae12b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae12b-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ComponentCategory" ) </span><span class="sxs-lookup"><span data-stu-id="ae12b-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComponentCategory")</span></span>
</dt> </dl>

<span data-ttu-id="ae12b-117">表示 COM 類別正在使用的元件類別之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="ae12b-117">Reference to the instance representing the component category being used by the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="ae12b-118">**元件**</span><span class="sxs-lookup"><span data-stu-id="ae12b-118">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae12b-119">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="ae12b-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="ae12b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae12b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae12b-121">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="ae12b-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="ae12b-122">使用相關聯的分類來參考表示 COM 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ae12b-122">Reference to the instance representing the COM class using the associated category.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae12b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae12b-123">Requirements</span></span>



| <span data-ttu-id="ae12b-124">需求</span><span class="sxs-lookup"><span data-stu-id="ae12b-124">Requirement</span></span> | <span data-ttu-id="ae12b-125">值</span><span class="sxs-lookup"><span data-stu-id="ae12b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae12b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae12b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ae12b-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae12b-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae12b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae12b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ae12b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae12b-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae12b-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="ae12b-130">Namespace</span></span><br/>                | <span data-ttu-id="ae12b-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae12b-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae12b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ae12b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae12b-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae12b-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae12b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ae12b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae12b-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae12b-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae12b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae12b-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae12b-137">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae12b-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

