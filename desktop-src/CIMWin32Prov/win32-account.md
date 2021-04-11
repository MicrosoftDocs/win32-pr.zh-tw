---
description: 包含執行 Windows 的電腦系統已知的使用者帳戶和群組帳戶的相關資訊。
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Win32_Account 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111377"
---
# <a name="win32_account-class"></a><span data-ttu-id="ccc5a-103">Win32 \_ 帳戶類別</span><span class="sxs-lookup"><span data-stu-id="ccc5a-103">Win32\_Account class</span></span>

<span data-ttu-id="ccc5a-104">**Win32 \_ 帳戶** 抽象 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)包含使用者帳戶和使用者帳戶的相關資訊，以及執行 Windows 的電腦系統已知的群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="ccc5a-105">Windows 網域辨識的使用者或組名是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="ccc5a-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ccc5a-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc5a-108">語法</span><span class="sxs-lookup"><span data-stu-id="ccc5a-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ccc5a-109">成員</span><span class="sxs-lookup"><span data-stu-id="ccc5a-109">Members</span></span>

<span data-ttu-id="ccc5a-110">**Win32 \_ 帳戶** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ccc5a-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="ccc5a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ccc5a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccc5a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ccc5a-112">Properties</span></span>

<span data-ttu-id="ccc5a-113">**Win32 \_ 帳戶** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccc5a-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-118">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-118">Short description of the object.</span></span>

<span data-ttu-id="ccc5a-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-123">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-124">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-124">Description of the object.</span></span>

<span data-ttu-id="ccc5a-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-126">**網域**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-129">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 函數 \| Domain" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-130">群組或使用者所屬之 Windows 網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="ccc5a-131">範例： "NA-SALES"</span><span class="sxs-lookup"><span data-stu-id="ccc5a-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-135">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ccc5a-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-136">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-136">Date and time that the object was installed.</span></span> <span data-ttu-id="ccc5a-137">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ccc5a-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-142">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ccc5a-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-143">若 **為 TRUE**，則會在本機電腦上定義帳戶。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="ccc5a-144">若只要取出本機電腦上定義的帳戶，請設計包含 "LocalAccount =**TRUE**" 條件的查詢。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-145">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-148">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Network Management 結構 \| 名稱" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-149">此類別的 **domain** 屬性所指定之網域上的 Windows 系統帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="ccc5a-150">這個屬性會覆寫繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)的 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-154">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Security 識別碼 (sid) " ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-155">此帳戶 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="ccc5a-156">SID 是變數長度的字串值，用來識別信任者。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="ccc5a-157">每個帳戶都有一個由授權單位所發行的唯一 SID (例如儲存在安全性資料庫中的 Windows 網域) 。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="ccc5a-158">當使用者登入時，系統會從資料庫抓取使用者的 SID，並將其放在使用者的存取權杖中。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="ccc5a-159">系統會在使用者的存取權杖中使用 SID，以在所有後續與 Windows 安全性的互動中識別使用者。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="ccc5a-160">使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="ccc5a-161">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-162">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-164">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 存取控制列舉類型 \| SID \_ 名稱 \_ 使用" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-165">列舉值，指定 (SID) 的安全識別碼類型。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="ccc5a-166">**SidTypeUser** (1) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="ccc5a-167">**SidTypeGroup** (2) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="ccc5a-168">**SidTypeDomain** (3) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="ccc5a-169">**SidTypeAlias** (4) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="ccc5a-170">**SidTypeWellKnownGroup** (5) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="ccc5a-171">**SidTypeDeletedAccount** (6) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="ccc5a-172">**SidTypeInvalid** (7) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="ccc5a-173">**SidTypeUnknown** (8) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="ccc5a-174">**SidTypeComputer** (9) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ccc5a-175">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccc5a-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ccc5a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccc5a-178">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ccc5a-179">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-179">Current status of the object.</span></span> <span data-ttu-id="ccc5a-180">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ccc5a-181">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但會在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="ccc5a-182">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ccc5a-183">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ccc5a-184">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ccc5a-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="ccc5a-186">值如下：</span><span class="sxs-lookup"><span data-stu-id="ccc5a-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ccc5a-187">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ccc5a-188">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ccc5a-189">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ccc5a-190">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ccc5a-191">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ccc5a-192">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ccc5a-193">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ccc5a-194">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ccc5a-195">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ccc5a-196">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ccc5a-197">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ccc5a-198">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ccc5a-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ccc5a-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ccc5a-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ccc5a-200">備註</span><span class="sxs-lookup"><span data-stu-id="ccc5a-200">Remarks</span></span>

<span data-ttu-id="ccc5a-201">**Win32 \_ 帳戶** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ccc5a-202">範例</span><span class="sxs-lookup"><span data-stu-id="ccc5a-202">Examples</span></span>

<span data-ttu-id="ccc5a-203">下列 PowerShell 程式碼會抓取本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="ccc5a-204">下列 PowerShell 程式碼會捕獲網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="ccc5a-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="ccc5a-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccc5a-205">Requirements</span></span>



| <span data-ttu-id="ccc5a-206">需求</span><span class="sxs-lookup"><span data-stu-id="ccc5a-206">Requirement</span></span> | <span data-ttu-id="ccc5a-207">值</span><span class="sxs-lookup"><span data-stu-id="ccc5a-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc5a-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccc5a-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc5a-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccc5a-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccc5a-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccc5a-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc5a-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccc5a-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccc5a-212">命名空間</span><span class="sxs-lookup"><span data-stu-id="ccc5a-212">Namespace</span></span><br/>                | <span data-ttu-id="ccc5a-213">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ccc5a-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ccc5a-214">MOF</span><span class="sxs-lookup"><span data-stu-id="ccc5a-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccc5a-215"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccc5a-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccc5a-216">DLL</span><span class="sxs-lookup"><span data-stu-id="ccc5a-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc5a-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc5a-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc5a-218">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccc5a-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc5a-219">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ccc5a-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="ccc5a-220">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ccc5a-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

