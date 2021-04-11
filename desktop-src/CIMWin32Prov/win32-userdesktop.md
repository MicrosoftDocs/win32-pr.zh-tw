---
description: Win32 \_ UserDesktop 關聯 WMI 類別會將其專屬的使用者帳戶和桌面設定相關聯。
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Win32_UserDesktop 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847143"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="78123-103">Win32 \_ UserDesktop 類別</span><span class="sxs-lookup"><span data-stu-id="78123-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="78123-104">**Win32 \_ UserDesktop** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將其專屬的使用者帳戶和桌面設定相關聯。</span><span class="sxs-lookup"><span data-stu-id="78123-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="78123-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="78123-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="78123-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="78123-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78123-107">語法</span><span class="sxs-lookup"><span data-stu-id="78123-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="78123-108">成員</span><span class="sxs-lookup"><span data-stu-id="78123-108">Members</span></span>

<span data-ttu-id="78123-109">**Win32 \_ UserDesktop** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78123-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="78123-110">屬性</span><span class="sxs-lookup"><span data-stu-id="78123-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78123-111">屬性</span><span class="sxs-lookup"><span data-stu-id="78123-111">Properties</span></span>

<span data-ttu-id="78123-112">**Win32 \_ UserDesktop** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78123-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78123-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="78123-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78123-114">資料類型： **Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="78123-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="78123-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78123-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78123-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ UserAccount" ) </span><span class="sxs-lookup"><span data-stu-id="78123-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="78123-117">代表使用者帳戶的實例參考，其桌面可由這個類別的 **Settings** 屬性自訂。</span><span class="sxs-lookup"><span data-stu-id="78123-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="78123-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="78123-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78123-119">資料類型： **Win32 \_ Desktop**</span><span class="sxs-lookup"><span data-stu-id="78123-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="78123-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78123-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78123-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Desktop" ) </span><span class="sxs-lookup"><span data-stu-id="78123-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="78123-122">代表用來自訂特定使用者帳戶桌面之桌面設定的實例參考。</span><span class="sxs-lookup"><span data-stu-id="78123-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78123-123">備註</span><span class="sxs-lookup"><span data-stu-id="78123-123">Remarks</span></span>

<span data-ttu-id="78123-124">**Win32 \_ UserDesktop** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="78123-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78123-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="78123-125">Requirements</span></span>



| <span data-ttu-id="78123-126">需求</span><span class="sxs-lookup"><span data-stu-id="78123-126">Requirement</span></span> | <span data-ttu-id="78123-127">值</span><span class="sxs-lookup"><span data-stu-id="78123-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78123-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78123-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78123-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78123-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78123-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78123-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78123-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78123-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78123-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="78123-132">Namespace</span></span><br/>                | <span data-ttu-id="78123-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="78123-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78123-134">MOF</span><span class="sxs-lookup"><span data-stu-id="78123-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78123-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="78123-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78123-136">DLL</span><span class="sxs-lookup"><span data-stu-id="78123-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78123-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78123-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78123-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78123-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78123-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="78123-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="78123-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="78123-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
