---
description: Win32 \_ UserAccount&\# 32;WMI 類別包含執行 Windows 的電腦系統上使用者帳戶的相關資訊。
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025861"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="d0a0d-103">Win32 \_ UserAccount 類別</span><span class="sxs-lookup"><span data-stu-id="d0a0d-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="d0a0d-104">**Win32 \_ UserAccount** [WMI 類別](../wmisdk/retrieving-a-class.md)包含執行 Windows 的電腦系統上使用者帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="d0a0d-105">由於 **名稱** 和 **網域** 都是索引鍵屬性，因此在大型網路上列舉 **Win32 \_ UserAccount** 可能會對效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="d0a0d-106">呼叫 **GetObject** 或查詢特定實例的影響較小。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="d0a0d-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d0a0d-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a0d-109">語法</span><span class="sxs-lookup"><span data-stu-id="d0a0d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d0a0d-110">成員</span><span class="sxs-lookup"><span data-stu-id="d0a0d-110">Members</span></span>

<span data-ttu-id="d0a0d-111">**Win32 \_ UserAccount** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d0a0d-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="d0a0d-112">方法</span><span class="sxs-lookup"><span data-stu-id="d0a0d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0a0d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d0a0d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0a0d-114">方法</span><span class="sxs-lookup"><span data-stu-id="d0a0d-114">Methods</span></span>

<span data-ttu-id="d0a0d-115">**Win32 \_ UserAccount** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="d0a0d-116">方法</span><span class="sxs-lookup"><span data-stu-id="d0a0d-116">Method</span></span>                                                     | <span data-ttu-id="d0a0d-117">描述</span><span class="sxs-lookup"><span data-stu-id="d0a0d-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="d0a0d-118">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="d0a0d-119">允許重新命名使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d0a0d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="d0a0d-120">Properties</span></span>

<span data-ttu-id="d0a0d-121">**Win32 \_ UserAccount** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0a0d-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-125">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ 旗標」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-126">描述 Windows 使用者帳戶特性的旗標。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="d0a0d-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**暫時重複的帳戶** (256) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="d0a0d-128">**UF \_ 暫存 \_ 重複 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="d0a0d-129">在另一個網域中具有主要帳戶之使用者的本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="d0a0d-130">此帳戶僅提供此網域的使用者存取權，而不是信任此網域的任何網域。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="d0a0d-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**一般帳戶** (512) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="d0a0d-132">**UF \_ 一般 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="d0a0d-133">代表一般使用者的預設帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="d0a0d-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span> (2048) 的 **域間信任帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="d0a0d-135">**每個 UF \_ 域 \_ 信任 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="d0a0d-136">適用于信任其他網域之系統網域的帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="d0a0d-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**工作站信任帳戶** (4096) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="d0a0d-138">**UF \_ 工作站 \_ 信任 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="d0a0d-139">電腦系統的電腦帳戶，執行屬於此網域成員的 Windows。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="d0a0d-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**伺服器信任帳戶** (8192) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="d0a0d-141">**UF \_ 伺服器 \_ 信任 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="d0a0d-142">屬於此網域成員的系統備份網域控制站帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0a0d-143">**標題**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-146">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-147">帳戶的網域和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-147">Domain and username of the account.</span></span>

<span data-ttu-id="d0a0d-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-152">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-153">帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-153">Description of the account.</span></span>

<span data-ttu-id="d0a0d-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-155">**Disabled**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-156">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-158">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| 使用者 \_ 資訊 \| UF \_ ACCOUNTDISABLE」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-159">Windows 使用者帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-160">**網域**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-163">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Domain" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| domainname" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-164">使用者帳戶所屬的 Windows 網功能變數名稱稱，例如： "NA-SALES"。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-168">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ full \_ name**" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-169">本機使用者的完整名稱，例如：「Dan Wilson」。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-171">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-173">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d0a0d-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-174">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-174">Date the object is installed.</span></span> <span data-ttu-id="d0a0d-175">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d0a0d-176">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-178">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-180">限定詞：已 [**修正**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d0a0d-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-181">若 **為 true**，則會在本機電腦上定義帳戶。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="d0a0d-182">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-183">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-186">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)的 \| **UF \_ 鎖定**」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-187">若 **為 true**，則表示使用者帳戶已被鎖定而無法使用 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-188">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-191">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| 名稱" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-192">此類別的 **網域** 屬性指定之網域上的 Windows 使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="d0a0d-193">範例： "danwilson"。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-193">Example: "danwilson".</span></span>

<span data-ttu-id="d0a0d-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-195">**PasswordChangeable**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)個 \| **UF \_ 密碼無法 \_ \_ 變更**」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-199">若 **為 true**，則可以變更此使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-201">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-203">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)的 \| **UF 未 \_ \_ 過期 \_**」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-204">若 **為 true**，則表示此使用者帳戶的密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-206">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-207">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d0a0d-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-208">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)個 \| **UF \_ 密碼 \_ NOTREQD**」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-209">若 **為 true**，則表示 Windows 使用者帳戶需要有密碼。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="d0a0d-210">如果 **為 false**，則此帳戶不需要密碼。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-214">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Security 識別碼 (sid) " ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-215">此帳戶 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="d0a0d-216">SID 是變數長度的字串值，可用來識別信任者。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="d0a0d-217">每個帳戶都有一個可供授權單位（例如 Windows 網域）發出的唯一 SID。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="d0a0d-218">SID 會儲存在安全性資料庫中。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-218">The SID is stored in the security database.</span></span> <span data-ttu-id="d0a0d-219">當使用者登入時，系統會從資料庫抓取使用者 SID，將 SID 放在使用者存取權杖中，然後使用使用者存取權杖中的 SID，在所有後續與 Windows 安全性的互動中識別使用者。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="d0a0d-220">每個 SID 都是使用者或群組的唯一識別碼，而且不同的使用者或群組不能有相同的 SID。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="d0a0d-221">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a0d-222">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-223">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-225">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 存取控制列舉類型 \| [**SID \_ 名稱 \_ 使用**](/windows/win32/api/winnt/ne-winnt-sid_name_use)" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-226">指定 SID 類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="d0a0d-227">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="d0a0d-228">**SidTypeUser** (1) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="d0a0d-229">**SidTypeGroup** (2) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="d0a0d-230">**SidTypeDomain** (3) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="d0a0d-231">**SidTypeAlias** (4) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="d0a0d-232">**SidTypeWellKnownGroup** (5) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="d0a0d-233">**SidTypeDeletedAccount** (6) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="d0a0d-234">**SidTypeInvalid** (7) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="d0a0d-235">**SidTypeUnknown** (8) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="d0a0d-236">**SidTypeComputer** (9) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0a0d-237">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a0d-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0a0d-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0a0d-240">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0a0d-241">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-241">Current status of an object.</span></span> <span data-ttu-id="d0a0d-242">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d0a0d-243">作業狀態包括：「確定」、「降級」和「Pred 失敗」，這是一種元素，例如可正常運作的智慧型硬碟，但在不久的未來會預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="d0a0d-244">Nonoperational 狀態包括：「錯誤」、「開始」、「停止」和「服務」，這可在磁片的鏡像重新同步處理期間套用、重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="d0a0d-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0a0d-246">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d0a0d-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0a0d-247">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0a0d-248">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0a0d-249">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0a0d-250">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0a0d-251">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0a0d-252">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0a0d-253">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0a0d-254">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0a0d-255">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0a0d-256">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0a0d-257">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0a0d-258">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d0a0d-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d0a0d-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0a0d-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d0a0d-260">備註</span><span class="sxs-lookup"><span data-stu-id="d0a0d-260">Remarks</span></span>

<span data-ttu-id="d0a0d-261">**Win32 \_ UserAccount** 類別衍生自 [**win32 \_ 帳戶**](win32-account.md)。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0a0d-262">嘗試寫入唯讀屬性時，不會傳回錯誤，而且屬性的值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d0a0d-263">範例</span><span class="sxs-lookup"><span data-stu-id="d0a0d-263">Examples</span></span>

<span data-ttu-id="d0a0d-264">在 TechNet 資源庫上使用 WMI VBScript 程式碼範例 [列出本機使用者帳戶](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) ，會使用 **Win32 \_ UserAccount** 來傳回在電腦上找到的本機使用者帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="d0a0d-265">將 [Sid 轉換為使用者帳戶，並將使用者帳戶轉換為 sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f)TechNet 資源庫上的 PowerShell 程式碼範例會使用 **Win32 \_ UserAccount** ，將 Sid 轉譯為使用者帳戶和/或使用者帳戶至 sid。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="d0a0d-266">下列 VBScript 程式碼範例會示範如何在本機電腦上取得使用者的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="d0a0d-267">全名是人類的語言名稱，例如，一個人可以有 "kensanchez" 的使用者名稱，而全名可能是 "Ken Sanchez"，所以您可以用真實的功能變數名稱和使用者名稱取代 "MyDomainName" 和 "MyUserName"。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="d0a0d-268">針對有效率的查詢，您必須同時指定 [網域] 和 [使用者名稱] 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="d0a0d-269">如果您是遠端電腦上的系統管理員，您可以指派 strComputer (的遠端電腦名稱稱，而不是 ".") ，然後使用下列腳本類型，從遠端電腦取得本機電腦上的使用者帳戶的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a0d-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="d0a0d-270">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0a0d-270">Requirements</span></span>



| <span data-ttu-id="d0a0d-271">需求</span><span class="sxs-lookup"><span data-stu-id="d0a0d-271">Requirement</span></span> | <span data-ttu-id="d0a0d-272">值</span><span class="sxs-lookup"><span data-stu-id="d0a0d-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a0d-273">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0a0d-273">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a0d-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0a0d-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0a0d-275">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0a0d-275">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a0d-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0a0d-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0a0d-277">命名空間</span><span class="sxs-lookup"><span data-stu-id="d0a0d-277">Namespace</span></span><br/>                | <span data-ttu-id="d0a0d-278">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d0a0d-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0a0d-279">MOF</span><span class="sxs-lookup"><span data-stu-id="d0a0d-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0a0d-280"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0d-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0a0d-281">DLL</span><span class="sxs-lookup"><span data-stu-id="d0a0d-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0a0d-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0d-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a0d-283">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0a0d-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a0d-284">**Win32 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="d0a0d-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="d0a0d-285">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="d0a0d-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
