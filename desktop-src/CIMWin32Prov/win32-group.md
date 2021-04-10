---
description: 代表群組帳戶的相關資料。
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Win32_Group 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111213"
---
# <a name="win32_group-class"></a><span data-ttu-id="bbf2e-103">Win32 \_ 群組類別</span><span class="sxs-lookup"><span data-stu-id="bbf2e-103">Win32\_Group class</span></span>

<span data-ttu-id="bbf2e-104">**Win32 \_ 群組** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表群組帳戶的相關資料。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="bbf2e-105">群組帳戶允許變更使用者清單的存取權限。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="bbf2e-106">範例： Marketing2。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-106">Example: Marketing2.</span></span>

<span data-ttu-id="bbf2e-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bbf2e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf2e-109">語法</span><span class="sxs-lookup"><span data-stu-id="bbf2e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="bbf2e-110">成員</span><span class="sxs-lookup"><span data-stu-id="bbf2e-110">Members</span></span>

<span data-ttu-id="bbf2e-111">**Win32 \_ 群組** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bbf2e-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="bbf2e-112">方法</span><span class="sxs-lookup"><span data-stu-id="bbf2e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bbf2e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bbf2e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bbf2e-114">方法</span><span class="sxs-lookup"><span data-stu-id="bbf2e-114">Methods</span></span>

<span data-ttu-id="bbf2e-115">**Win32 \_ 群組** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="bbf2e-116">方法</span><span class="sxs-lookup"><span data-stu-id="bbf2e-116">Method</span></span>                                               | <span data-ttu-id="bbf2e-117">描述</span><span class="sxs-lookup"><span data-stu-id="bbf2e-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="bbf2e-118">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="bbf2e-119">變更組名。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bbf2e-120">屬性</span><span class="sxs-lookup"><span data-stu-id="bbf2e-120">Properties</span></span>

<span data-ttu-id="bbf2e-121">**Win32 \_ 群組** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbf2e-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-125">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-126">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-126">A short textual description of the object.</span></span>

<span data-ttu-id="bbf2e-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-131">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-132">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-132">A textual description of the object.</span></span>

<span data-ttu-id="bbf2e-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-134">**網域**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-137">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Domain" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 函數 \| domainname" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-138">群組帳戶所屬之 Windows 網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="bbf2e-139">範例： "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="bbf2e-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-141">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="bbf2e-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-144">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-144">Indicates when the object was installed.</span></span> <span data-ttu-id="bbf2e-145">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bbf2e-146">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-150">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bbf2e-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-151">若 **為 TRUE**，則會在本機電腦上定義帳戶。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="bbf2e-152">若只要取出本機電腦上定義的帳戶，請設計包含 "LocalAccount =**TRUE**" 條件的查詢。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="bbf2e-153">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-154">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-157">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| 名稱" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-158">此類別的 **domain** 屬性所指定之網域上的 Windows 群組帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-162">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Security 識別碼 (sid) " ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-163">此帳戶 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="bbf2e-164">SID 是變數長度的字串值，用來識別信任者。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="bbf2e-165">每個帳戶都有一個由授權單位所發行的唯一 SID (例如儲存在安全性資料庫中的 Windows 網域) 。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="bbf2e-166">當使用者登入時，系統會從資料庫抓取使用者的 SID，並將其放在使用者的存取權杖中。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="bbf2e-167">系統會在使用者的存取權杖中使用 SID，以在所有後續與 Windows 安全性的互動中識別使用者。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="bbf2e-168">使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="bbf2e-169">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbf2e-170">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-171">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-173">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 存取控制列舉類型 \| SID \_ 名稱 \_ 使用" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-174">列舉值，指定 (SID) 的安全識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="bbf2e-175">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="bbf2e-176">**SidTypeUser** (1) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="bbf2e-177">**SidTypeGroup** (2) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="bbf2e-178">**SidTypeDomain** (3) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="bbf2e-179">**SidTypeAlias** (4) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="bbf2e-180">**SidTypeWellKnownGroup** (5) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="bbf2e-181">**SidTypeDeletedAccount** (6) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="bbf2e-182">**SidTypeInvalid** (7) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="bbf2e-183">**SidTypeUnknown** (8) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="bbf2e-184">**SidTypeComputer** (9) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbf2e-185">**狀態**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbf2e-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bbf2e-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbf2e-188">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bbf2e-189">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="bbf2e-190">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="bbf2e-191">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="bbf2e-192">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="bbf2e-193">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bbf2e-194">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bbf2e-195">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bbf2e-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bbf2e-197">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="bbf2e-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bbf2e-198">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bbf2e-199">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bbf2e-200">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbf2e-201">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bbf2e-202">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bbf2e-203">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bbf2e-204">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bbf2e-205">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bbf2e-206">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bbf2e-207">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bbf2e-208">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bbf2e-209">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="bbf2e-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="bbf2e-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bbf2e-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="bbf2e-211">備註</span><span class="sxs-lookup"><span data-stu-id="bbf2e-211">Remarks</span></span>

<span data-ttu-id="bbf2e-212">**Win32 \_ 群組** 類別衍生自 [**win32 \_ 帳戶**](win32-account.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bbf2e-213">範例</span><span class="sxs-lookup"><span data-stu-id="bbf2e-213">Examples</span></span>

<span data-ttu-id="bbf2e-214">下列程式碼是取自 TechNet 資源庫上使用 WMI VBScript 程式碼範例的 [清單本機群組](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) ，會使用 **Win32 \_ 群組** 來傳回電腦上找到之本機群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bbf2e-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="bbf2e-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbf2e-215">Requirements</span></span>



| <span data-ttu-id="bbf2e-216">需求</span><span class="sxs-lookup"><span data-stu-id="bbf2e-216">Requirement</span></span> | <span data-ttu-id="bbf2e-217">值</span><span class="sxs-lookup"><span data-stu-id="bbf2e-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf2e-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbf2e-218">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf2e-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbf2e-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbf2e-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbf2e-220">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf2e-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbf2e-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbf2e-222">命名空間</span><span class="sxs-lookup"><span data-stu-id="bbf2e-222">Namespace</span></span><br/>                | <span data-ttu-id="bbf2e-223">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bbf2e-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bbf2e-224">MOF</span><span class="sxs-lookup"><span data-stu-id="bbf2e-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbf2e-225"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbf2e-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbf2e-226">DLL</span><span class="sxs-lookup"><span data-stu-id="bbf2e-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbf2e-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf2e-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf2e-228">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbf2e-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf2e-229">**Win32 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="bbf2e-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="bbf2e-230">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bbf2e-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

