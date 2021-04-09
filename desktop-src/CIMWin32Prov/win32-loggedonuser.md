---
description: Win32 \_ LoggedOnUser 關聯 WMI 類別會建立會話與使用者帳戶的關聯。
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847527"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="1271d-103">Win32 \_ LoggedOnUser 類別</span><span class="sxs-lookup"><span data-stu-id="1271d-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="1271d-104">**Win32 \_ LoggedOnUser** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立會話與使用者帳戶的關聯。</span><span class="sxs-lookup"><span data-stu-id="1271d-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="1271d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1271d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1271d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1271d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1271d-107">語法</span><span class="sxs-lookup"><span data-stu-id="1271d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1271d-108">成員</span><span class="sxs-lookup"><span data-stu-id="1271d-108">Members</span></span>

<span data-ttu-id="1271d-109">**Win32 \_ LoggedOnUser** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1271d-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="1271d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1271d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1271d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1271d-111">Properties</span></span>

<span data-ttu-id="1271d-112">**Win32 \_ LoggedOnUser** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1271d-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1271d-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="1271d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1271d-114">資料類型： **Win32 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="1271d-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="1271d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1271d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1271d-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) () ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1271d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1271d-117">[**Win32 \_ 帳戶**](win32-account.md)，描述在此會話起始時使用的帳戶。</span><span class="sxs-lookup"><span data-stu-id="1271d-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="1271d-118">帳戶可以是使用者帳戶或系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="1271d-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="1271d-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="1271d-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1271d-120">資料類型： **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="1271d-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="1271d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1271d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1271d-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (相依) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1271d-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1271d-123">[**Win32 \_ LogonSession**](win32-logonsessionmappeddisk.md) ，描述帳戶目前所使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1271d-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1271d-124">備註</span><span class="sxs-lookup"><span data-stu-id="1271d-124">Remarks</span></span>

<span data-ttu-id="1271d-125">**Win32 \_ LoggedOnUser** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="1271d-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1271d-126">範例</span><span class="sxs-lookup"><span data-stu-id="1271d-126">Examples</span></span>

<span data-ttu-id="1271d-127">[Loggedonuser 函式](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a)PowerShell 範例會取得本機或遠端電腦上已登入的使用者，以及會話資訊。</span><span class="sxs-lookup"><span data-stu-id="1271d-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1271d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1271d-128">Requirements</span></span>



| <span data-ttu-id="1271d-129">需求</span><span class="sxs-lookup"><span data-stu-id="1271d-129">Requirement</span></span> | <span data-ttu-id="1271d-130">值</span><span class="sxs-lookup"><span data-stu-id="1271d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1271d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1271d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1271d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1271d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1271d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1271d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1271d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1271d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1271d-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="1271d-135">Namespace</span></span><br/>                | <span data-ttu-id="1271d-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1271d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1271d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1271d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1271d-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1271d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1271d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1271d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1271d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1271d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1271d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1271d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1271d-142">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="1271d-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="1271d-143">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1271d-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

