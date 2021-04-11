---
description: Win32 \_ ClassicCOMClassSettings 關聯 WMI 類別會將元件物件模型與 com) 類別 (，以及用來設定 com 類別實例的設定相關聯。
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847081"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="b360b-103">Win32 \_ ClassicCOMClassSettings 類別</span><span class="sxs-lookup"><span data-stu-id="b360b-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="b360b-104">**Win32 \_ ClassicCOMClassSettings** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將元件物件模型與 com) 類別 (，以及用來設定 com 類別實例的設定相關聯。</span><span class="sxs-lookup"><span data-stu-id="b360b-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="b360b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b360b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b360b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b360b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b360b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b360b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="b360b-108">成員</span><span class="sxs-lookup"><span data-stu-id="b360b-108">Members</span></span>

<span data-ttu-id="b360b-109">**Win32 \_ ClassicCOMClassSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b360b-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="b360b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b360b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b360b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b360b-111">Properties</span></span>

<span data-ttu-id="b360b-112">**Win32 \_ ClassicCOMClassSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b360b-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b360b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b360b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b360b-114">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="b360b-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="b360b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b360b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b360b-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="b360b-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="b360b-117">[**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md) ，表示套用設定的 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="b360b-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="b360b-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="b360b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b360b-119">資料類型： **Win32 \_ ClassicCOMClassSetting**</span><span class="sxs-lookup"><span data-stu-id="b360b-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="b360b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b360b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b360b-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "設定" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClassSetting" ) </span><span class="sxs-lookup"><span data-stu-id="b360b-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="b360b-122">[**Win32 \_ ClassicCOMClassSetting**](win32-classiccomclasssetting.md) ，表示與 COM 類別相關聯的設定。</span><span class="sxs-lookup"><span data-stu-id="b360b-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b360b-123">備註</span><span class="sxs-lookup"><span data-stu-id="b360b-123">Remarks</span></span>

<span data-ttu-id="b360b-124">**Win32 \_ ClassicCOMClassSettings** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="b360b-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b360b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b360b-125">Requirements</span></span>



| <span data-ttu-id="b360b-126">需求</span><span class="sxs-lookup"><span data-stu-id="b360b-126">Requirement</span></span> | <span data-ttu-id="b360b-127">值</span><span class="sxs-lookup"><span data-stu-id="b360b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b360b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b360b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b360b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b360b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b360b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b360b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b360b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b360b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b360b-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b360b-132">Namespace</span></span><br/>                | <span data-ttu-id="b360b-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b360b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b360b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b360b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b360b-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b360b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b360b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b360b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b360b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b360b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b360b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b360b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b360b-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="b360b-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="b360b-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b360b-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

