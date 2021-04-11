---
description: 此類別代表作業系統和適用于電腦上磁片的 autochk 設定之間的關聯。請注意，此設定會與作業系統相關聯，而不是電腦系統，因為電腦上可能已安裝一或多個作業系統，每個作業系統都有自己的 autochk 設定。
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111349"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="7b3e3-103">Win32 \_ OperatingSystemAutochkSetting 類別</span><span class="sxs-lookup"><span data-stu-id="7b3e3-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="7b3e3-104">此類別代表作業系統和適用于電腦上磁片的 autochk 設定之間的關聯。請注意，此設定會與作業系統相關聯，而不是電腦系統，因為電腦上可能已安裝一或多個作業系統，每個作業系統都有自己的 autochk 設定。</span><span class="sxs-lookup"><span data-stu-id="7b3e3-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="7b3e3-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b3e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3e3-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b3e3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="7b3e3-107">成員</span><span class="sxs-lookup"><span data-stu-id="7b3e3-107">Members</span></span>

<span data-ttu-id="7b3e3-108">**Win32 \_ OperatingSystemAutochkSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b3e3-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="7b3e3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7b3e3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b3e3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7b3e3-110">Properties</span></span>

<span data-ttu-id="7b3e3-111">**Win32 \_ OperatingSystemAutochkSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b3e3-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b3e3-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b3e3-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b3e3-113">資料類型： **Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="7b3e3-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7b3e3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b3e3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b3e3-115">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="7b3e3-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="7b3e3-116">TBD</span><span class="sxs-lookup"><span data-stu-id="7b3e3-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="7b3e3-117">**設定**</span><span class="sxs-lookup"><span data-stu-id="7b3e3-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b3e3-118">資料類型： **Win32 \_ AutochkSetting**</span><span class="sxs-lookup"><span data-stu-id="7b3e3-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="7b3e3-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b3e3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b3e3-120">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**金鑰**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="7b3e3-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="7b3e3-121">TBD</span><span class="sxs-lookup"><span data-stu-id="7b3e3-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b3e3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b3e3-122">Requirements</span></span>



| <span data-ttu-id="7b3e3-123">需求</span><span class="sxs-lookup"><span data-stu-id="7b3e3-123">Requirement</span></span> | <span data-ttu-id="7b3e3-124">值</span><span class="sxs-lookup"><span data-stu-id="7b3e3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3e3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b3e3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3e3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b3e3-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b3e3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b3e3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3e3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b3e3-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b3e3-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b3e3-129">Namespace</span></span><br/>                | <span data-ttu-id="7b3e3-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b3e3-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b3e3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7b3e3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b3e3-132"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b3e3-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b3e3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7b3e3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b3e3-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b3e3-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3e3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b3e3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3e3-136">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="7b3e3-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
