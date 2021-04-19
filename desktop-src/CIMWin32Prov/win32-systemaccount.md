---
description: Win32 \_ SystemAccount&\# 8194;WMI 類別代表系統帳戶。
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Win32_SystemAccount 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972571"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="7ba76-103">Win32 \_ SystemAccount 類別</span><span class="sxs-lookup"><span data-stu-id="7ba76-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="7ba76-104">**Win32 \_ SystemAccount** [WMI 類別](../wmisdk/retrieving-a-class.md)代表系統帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ba76-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="7ba76-105">系統帳戶是由作業系統和服務所使用。</span><span class="sxs-lookup"><span data-stu-id="7ba76-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="7ba76-106">Windows 中有許多服務和進程需要在內部登入，例如在 Windows 安裝期間。</span><span class="sxs-lookup"><span data-stu-id="7ba76-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="7ba76-107">系統帳戶是針對該目的所設計。</span><span class="sxs-lookup"><span data-stu-id="7ba76-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="7ba76-108">系統帳戶是未顯示在使用者管理員中的內部帳戶，無法新增至任何群組，也無法將使用者權限指派給該帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ba76-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="7ba76-109">不過，系統帳戶會顯示在 [檔案管理員] 中的 NTFS 檔案系統磁片區，該磁片區位於 [安全性] 功能表的 [許可權] 區段中。</span><span class="sxs-lookup"><span data-stu-id="7ba76-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="7ba76-110">根據預設，系統帳戶會被授與 NTFS 檔案系統磁片區上所有檔案的完整控制權，這表示系統帳戶具有與系統管理員帳戶相同的功能許可權。</span><span class="sxs-lookup"><span data-stu-id="7ba76-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="7ba76-111">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7ba76-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7ba76-112">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="7ba76-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba76-113">語法</span><span class="sxs-lookup"><span data-stu-id="7ba76-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
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

## <a name="members"></a><span data-ttu-id="7ba76-114">成員</span><span class="sxs-lookup"><span data-stu-id="7ba76-114">Members</span></span>

<span data-ttu-id="7ba76-115">**Win32 \_ SystemAccount** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ba76-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="7ba76-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7ba76-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ba76-117">屬性</span><span class="sxs-lookup"><span data-stu-id="7ba76-117">Properties</span></span>

<span data-ttu-id="7ba76-118">**Win32 \_ SystemAccount** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7ba76-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ba76-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="7ba76-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-122">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-123">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="7ba76-123">A short textual description of the object.</span></span>

<span data-ttu-id="7ba76-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ba76-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="7ba76-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-128">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-129">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7ba76-129">A textual description of the object.</span></span>

<span data-ttu-id="7ba76-130">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ba76-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-131">**網域**</span><span class="sxs-lookup"><span data-stu-id="7ba76-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-134">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Domain" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| domainname" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-135">系統帳戶所屬之 Windows 網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ba76-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="7ba76-136">範例： "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="7ba76-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7ba76-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-138">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7ba76-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-140">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="7ba76-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-141">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="7ba76-141">Indicates when the object was installed.</span></span> <span data-ttu-id="7ba76-142">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="7ba76-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7ba76-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ba76-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="7ba76-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7ba76-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-147">限定詞：已 [**修正**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-148">若 **為 TRUE**，則會在本機電腦上定義帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ba76-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="7ba76-149">若只要取出本機電腦上定義的帳戶，請設計包含 "LocalAccount =**TRUE**" 條件的查詢。</span><span class="sxs-lookup"><span data-stu-id="7ba76-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="7ba76-150">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="7ba76-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-151">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7ba76-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-154">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| 名稱" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-155">此類別的 **domain** 屬性所指定之網域上的 Windows 系統帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7ba76-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="7ba76-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-159">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Security 識別碼 (sid) " ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-160">此帳戶 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ba76-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="7ba76-161">SID 是變數長度的字串值，用來識別信任者。</span><span class="sxs-lookup"><span data-stu-id="7ba76-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="7ba76-162">每個帳戶都有一個由授權單位所發行的唯一 SID (例如儲存在安全性資料庫中的 Windows 網域) 。</span><span class="sxs-lookup"><span data-stu-id="7ba76-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="7ba76-163">當使用者登入時，系統會從資料庫抓取使用者的 SID，並將其放在使用者的存取權杖中。</span><span class="sxs-lookup"><span data-stu-id="7ba76-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="7ba76-164">系統會在使用者的存取權杖中使用 SID，以在所有後續與 Windows 安全性的互動中識別使用者。</span><span class="sxs-lookup"><span data-stu-id="7ba76-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="7ba76-165">使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。</span><span class="sxs-lookup"><span data-stu-id="7ba76-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="7ba76-166">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="7ba76-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ba76-167">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="7ba76-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-168">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7ba76-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-170">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 存取控制列舉類型 \| SID \_ 名稱 \_ 使用" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-171">列舉值，指定 (SID) 的安全識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="7ba76-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="7ba76-172">這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="7ba76-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="7ba76-173">**SidTypeUser** (1) </span><span class="sxs-lookup"><span data-stu-id="7ba76-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="7ba76-174">**SidTypeGroup** (2) </span><span class="sxs-lookup"><span data-stu-id="7ba76-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="7ba76-175">**SidTypeDomain** (3) </span><span class="sxs-lookup"><span data-stu-id="7ba76-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="7ba76-176">**SidTypeAlias** (4) </span><span class="sxs-lookup"><span data-stu-id="7ba76-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="7ba76-177">**SidTypeWellKnownGroup** (5) </span><span class="sxs-lookup"><span data-stu-id="7ba76-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="7ba76-178">**SidTypeDeletedAccount** (6) </span><span class="sxs-lookup"><span data-stu-id="7ba76-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="7ba76-179">**SidTypeInvalid** (7) </span><span class="sxs-lookup"><span data-stu-id="7ba76-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="7ba76-180">**SidTypeUnknown** (8) </span><span class="sxs-lookup"><span data-stu-id="7ba76-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="7ba76-181">**SidTypeComputer** (9) </span><span class="sxs-lookup"><span data-stu-id="7ba76-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ba76-182">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7ba76-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba76-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ba76-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ba76-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba76-185">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7ba76-186">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="7ba76-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="7ba76-187">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="7ba76-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7ba76-188">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="7ba76-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7ba76-189">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="7ba76-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7ba76-190">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="7ba76-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7ba76-191">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="7ba76-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7ba76-192">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="7ba76-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7ba76-193">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="7ba76-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7ba76-194">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="7ba76-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7ba76-195">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7ba76-196">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7ba76-197">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ba76-198">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7ba76-199">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7ba76-200">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7ba76-201">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7ba76-202">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7ba76-203">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7ba76-204">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7ba76-205">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7ba76-206">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="7ba76-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7ba76-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7ba76-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7ba76-208">備註</span><span class="sxs-lookup"><span data-stu-id="7ba76-208">Remarks</span></span>

<span data-ttu-id="7ba76-209">**Win32 \_ SystemAccount** 類別衍生自 [**win32 \_ 帳戶**](win32-account.md)。</span><span class="sxs-lookup"><span data-stu-id="7ba76-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba76-210">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ba76-210">Requirements</span></span>



| <span data-ttu-id="7ba76-211">需求</span><span class="sxs-lookup"><span data-stu-id="7ba76-211">Requirement</span></span> | <span data-ttu-id="7ba76-212">值</span><span class="sxs-lookup"><span data-stu-id="7ba76-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba76-213">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ba76-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba76-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ba76-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ba76-215">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ba76-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba76-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ba76-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ba76-217">命名空間</span><span class="sxs-lookup"><span data-stu-id="7ba76-217">Namespace</span></span><br/>                | <span data-ttu-id="7ba76-218">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7ba76-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ba76-219">MOF</span><span class="sxs-lookup"><span data-stu-id="7ba76-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ba76-220"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ba76-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ba76-221">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba76-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba76-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba76-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ba76-223">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ba76-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba76-224">**Win32 \_ 帳戶**</span><span class="sxs-lookup"><span data-stu-id="7ba76-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="7ba76-225">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="7ba76-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
