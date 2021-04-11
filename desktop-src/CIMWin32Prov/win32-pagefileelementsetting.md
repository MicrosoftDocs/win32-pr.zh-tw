---
description: Win32 \_ PageFileElementSetting 關聯 WMI 類別會將分頁檔案的初始設定以及這些設定在正常使用期間的狀態產生關聯。
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Win32_PageFileElementSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936447"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="944e0-103">Win32 \_ PageFileElementSetting 類別</span><span class="sxs-lookup"><span data-stu-id="944e0-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="944e0-104">**Win32 \_ PageFileElementSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將分頁檔案的初始設定以及這些設定在正常使用期間的狀態產生關聯。</span><span class="sxs-lookup"><span data-stu-id="944e0-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="944e0-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="944e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="944e0-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="944e0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="944e0-107">語法</span><span class="sxs-lookup"><span data-stu-id="944e0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="944e0-108">成員</span><span class="sxs-lookup"><span data-stu-id="944e0-108">Members</span></span>

<span data-ttu-id="944e0-109">**Win32 \_ PageFileElementSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="944e0-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="944e0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="944e0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="944e0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="944e0-111">Properties</span></span>

<span data-ttu-id="944e0-112">**Win32 \_ PageFileElementSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="944e0-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="944e0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="944e0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944e0-114">資料類型： **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="944e0-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="944e0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="944e0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="944e0-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PageFileUsage" ) </span><span class="sxs-lookup"><span data-stu-id="944e0-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="944e0-117">當 Win32 系統正在使用中時，代表頁面檔案屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="944e0-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="944e0-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="944e0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="944e0-119">資料類型： **Win32 \_ PageFileSetting**</span><span class="sxs-lookup"><span data-stu-id="944e0-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="944e0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="944e0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="944e0-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PageFileSetting" ) </span><span class="sxs-lookup"><span data-stu-id="944e0-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="944e0-122">當 Win32 系統啟動時，代表分頁檔初始設定的實例參考。</span><span class="sxs-lookup"><span data-stu-id="944e0-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="944e0-123">備註</span><span class="sxs-lookup"><span data-stu-id="944e0-123">Remarks</span></span>

<span data-ttu-id="944e0-124">**Win32 \_ PageFileElementSetting** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="944e0-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="944e0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="944e0-125">Requirements</span></span>



| <span data-ttu-id="944e0-126">需求</span><span class="sxs-lookup"><span data-stu-id="944e0-126">Requirement</span></span> | <span data-ttu-id="944e0-127">值</span><span class="sxs-lookup"><span data-stu-id="944e0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="944e0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="944e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="944e0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="944e0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="944e0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="944e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="944e0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="944e0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="944e0-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="944e0-132">Namespace</span></span><br/>                | <span data-ttu-id="944e0-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="944e0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="944e0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="944e0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="944e0-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="944e0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="944e0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="944e0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="944e0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="944e0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="944e0-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="944e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="944e0-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="944e0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="944e0-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="944e0-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
