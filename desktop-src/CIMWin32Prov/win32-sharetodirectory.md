---
description: Win32 \_ ShareToDirectory 關聯 WMI 類別會將電腦系統上的共用資源與其對應的目錄相關聯。
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688588"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="d8e65-103">Win32 \_ ShareToDirectory 類別</span><span class="sxs-lookup"><span data-stu-id="d8e65-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="d8e65-104">**Win32 \_ ShareToDirectory** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統上的共用資源與其對應的目錄相關聯。</span><span class="sxs-lookup"><span data-stu-id="d8e65-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="d8e65-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d8e65-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d8e65-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="d8e65-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e65-107">語法</span><span class="sxs-lookup"><span data-stu-id="d8e65-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="d8e65-108">成員</span><span class="sxs-lookup"><span data-stu-id="d8e65-108">Members</span></span>

<span data-ttu-id="d8e65-109">**Win32 \_ ShareToDirectory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8e65-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="d8e65-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d8e65-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8e65-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d8e65-111">Properties</span></span>

<span data-ttu-id="d8e65-112">**Win32 \_ ShareToDirectory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8e65-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8e65-113">**共用**</span><span class="sxs-lookup"><span data-stu-id="d8e65-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e65-114">資料類型： **Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="d8e65-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="d8e65-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8e65-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e65-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Share" ) </span><span class="sxs-lookup"><span data-stu-id="d8e65-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="d8e65-117">此實例的參考，代表可透過目錄取得之共用資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="d8e65-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="d8e65-118">**SharedElement**</span><span class="sxs-lookup"><span data-stu-id="d8e65-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8e65-119">資料類型： **CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="d8e65-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="d8e65-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8e65-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8e65-121">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ Directory" ) </span><span class="sxs-lookup"><span data-stu-id="d8e65-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="d8e65-122">實例的參考，代表已對應至共用資源的目錄屬性。</span><span class="sxs-lookup"><span data-stu-id="d8e65-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8e65-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8e65-123">Requirements</span></span>



| <span data-ttu-id="d8e65-124">需求</span><span class="sxs-lookup"><span data-stu-id="d8e65-124">Requirement</span></span> | <span data-ttu-id="d8e65-125">值</span><span class="sxs-lookup"><span data-stu-id="d8e65-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e65-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8e65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e65-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8e65-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8e65-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8e65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e65-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8e65-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8e65-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8e65-130">Namespace</span></span><br/>                | <span data-ttu-id="d8e65-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d8e65-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8e65-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d8e65-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8e65-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8e65-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8e65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8e65-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e65-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e65-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8e65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e65-137">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="d8e65-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
