---
description: Win32 \_ GroupUser 關聯 WMI 類別會關聯群組和屬於該群組成員的帳戶。
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Win32_GroupUser 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468436"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="bddfb-103">Win32 \_ GroupUser 類別</span><span class="sxs-lookup"><span data-stu-id="bddfb-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="bddfb-104">**Win32 \_ GroupUser** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯群組和屬於該群組成員的帳戶。</span><span class="sxs-lookup"><span data-stu-id="bddfb-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="bddfb-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bddfb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bddfb-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bddfb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddfb-107">語法</span><span class="sxs-lookup"><span data-stu-id="bddfb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="bddfb-108">成員</span><span class="sxs-lookup"><span data-stu-id="bddfb-108">Members</span></span>

<span data-ttu-id="bddfb-109">**Win32 \_ GroupUser** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bddfb-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="bddfb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bddfb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bddfb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bddfb-111">Properties</span></span>

<span data-ttu-id="bddfb-112">**Win32 \_ GroupUser** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bddfb-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bddfb-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bddfb-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bddfb-114">資料類型： **Win32 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="bddfb-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="bddfb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bddfb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bddfb-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ Group" ) </span><span class="sxs-lookup"><span data-stu-id="bddfb-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="bddfb-117">代表帳戶所屬群組之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="bddfb-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="bddfb-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bddfb-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bddfb-119">資料類型： **Win32 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="bddfb-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="bddfb-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bddfb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bddfb-121">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ Account" ) </span><span class="sxs-lookup"><span data-stu-id="bddfb-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="bddfb-122">此實例的參考，代表屬於帳戶群組的使用者或系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="bddfb-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bddfb-123">備註</span><span class="sxs-lookup"><span data-stu-id="bddfb-123">Remarks</span></span>

<span data-ttu-id="bddfb-124">**Win32 \_ GroupUser** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="bddfb-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bddfb-125">範例</span><span class="sxs-lookup"><span data-stu-id="bddfb-125">Examples</span></span>

<span data-ttu-id="bddfb-126">如需使用 Win32 \_ GroupUser 來取出本機群組成員清單的 PowerShell 範例，請參閱 TechNet 資源庫上的 [使用 WMI 和 PowerShell 範例列出遠端電腦上的本機群組成員](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) 。</span><span class="sxs-lookup"><span data-stu-id="bddfb-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="bddfb-127">TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ GroupUser** 類別，從多部遠端電腦抓取使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="bddfb-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddfb-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddfb-128">Requirements</span></span>



| <span data-ttu-id="bddfb-129">需求</span><span class="sxs-lookup"><span data-stu-id="bddfb-129">Requirement</span></span> | <span data-ttu-id="bddfb-130">值</span><span class="sxs-lookup"><span data-stu-id="bddfb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bddfb-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bddfb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bddfb-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bddfb-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bddfb-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bddfb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bddfb-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bddfb-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bddfb-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="bddfb-135">Namespace</span></span><br/>                | <span data-ttu-id="bddfb-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bddfb-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bddfb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="bddfb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bddfb-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bddfb-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bddfb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bddfb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bddfb-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bddfb-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddfb-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddfb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddfb-142">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="bddfb-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="bddfb-143">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bddfb-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

