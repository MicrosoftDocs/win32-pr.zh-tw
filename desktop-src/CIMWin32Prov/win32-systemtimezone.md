---
description: Win32 \_ SystemTimeZone 關聯 WMI 類別會將電腦系統和時區產生關聯。
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Win32_SystemTimeZone 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847310"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="16435-103">Win32 \_ SystemTimeZone 類別</span><span class="sxs-lookup"><span data-stu-id="16435-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="16435-104">**Win32 \_ SystemTimeZone** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統和時區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="16435-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="16435-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16435-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="16435-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="16435-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16435-107">語法</span><span class="sxs-lookup"><span data-stu-id="16435-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="16435-108">成員</span><span class="sxs-lookup"><span data-stu-id="16435-108">Members</span></span>

<span data-ttu-id="16435-109">**Win32 \_ SystemTimeZone** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16435-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="16435-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16435-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16435-111">屬性</span><span class="sxs-lookup"><span data-stu-id="16435-111">Properties</span></span>

<span data-ttu-id="16435-112">**Win32 \_ SystemTimeZone** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16435-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16435-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="16435-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16435-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="16435-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="16435-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16435-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16435-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI Win32 \| \_ " ) </span><span class="sxs-lookup"><span data-stu-id="16435-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="16435-117">實例的參考，代表電腦系統追蹤系統時區。</span><span class="sxs-lookup"><span data-stu-id="16435-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="16435-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="16435-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16435-119">資料類型： **Win32 \_ 時區**</span><span class="sxs-lookup"><span data-stu-id="16435-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="16435-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16435-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16435-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ 時區" ) </span><span class="sxs-lookup"><span data-stu-id="16435-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="16435-122">此實例的參考，代表電腦系統所追蹤的時區屬性。</span><span class="sxs-lookup"><span data-stu-id="16435-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16435-123">備註</span><span class="sxs-lookup"><span data-stu-id="16435-123">Remarks</span></span>

<span data-ttu-id="16435-124">**Win32 \_ SystemTimeZone** 類別衍生自 [**win32 \_ SystemSetting**](win32-systemsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="16435-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16435-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="16435-125">Requirements</span></span>



| <span data-ttu-id="16435-126">需求</span><span class="sxs-lookup"><span data-stu-id="16435-126">Requirement</span></span> | <span data-ttu-id="16435-127">值</span><span class="sxs-lookup"><span data-stu-id="16435-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16435-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16435-128">Minimum supported client</span></span><br/> | <span data-ttu-id="16435-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16435-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16435-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16435-130">Minimum supported server</span></span><br/> | <span data-ttu-id="16435-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16435-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16435-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="16435-132">Namespace</span></span><br/>                | <span data-ttu-id="16435-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="16435-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16435-134">MOF</span><span class="sxs-lookup"><span data-stu-id="16435-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16435-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="16435-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16435-136">DLL</span><span class="sxs-lookup"><span data-stu-id="16435-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16435-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16435-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16435-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16435-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16435-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="16435-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="16435-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="16435-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
