---
description: Win32 \_ NetworkLoginProfile&\# 8194;WMI 類別代表執行 Windows 的電腦系統上特定使用者的網路登入資訊。
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970542"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="88f35-103">Win32 \_ NetworkLoginProfile 類別</span><span class="sxs-lookup"><span data-stu-id="88f35-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="88f35-104">**Win32 \_ NetworkLoginProfile** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上特定使用者的網路登入資訊。</span><span class="sxs-lookup"><span data-stu-id="88f35-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="88f35-105">這包括但不限於密碼狀態、存取權限、磁片配額和登入目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="88f35-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="88f35-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="88f35-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f35-107">語法</span><span class="sxs-lookup"><span data-stu-id="88f35-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="88f35-108">成員</span><span class="sxs-lookup"><span data-stu-id="88f35-108">Members</span></span>

<span data-ttu-id="88f35-109">**Win32 \_ NetworkLoginProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88f35-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="88f35-110">屬性</span><span class="sxs-lookup"><span data-stu-id="88f35-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88f35-111">屬性</span><span class="sxs-lookup"><span data-stu-id="88f35-111">Properties</span></span>

<span data-ttu-id="88f35-112">**Win32 \_ NetworkLoginProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88f35-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88f35-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="88f35-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-114">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88f35-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 帳戶 \_ 到期」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-117">帳戶將到期。</span><span class="sxs-lookup"><span data-stu-id="88f35-117">Account will expire.</span></span> <span data-ttu-id="88f35-118">此值的計算方式是從00:00:00 年1月 1970 1 日起經過的秒數開始計算，並以下列格式設定： yyyymmddhhmmss.ffffff. mmmmmm sutc。</span><span class="sxs-lookup"><span data-stu-id="88f35-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="88f35-119">範例： 20521201000230.000000 000</span><span class="sxs-lookup"><span data-stu-id="88f35-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="88f35-120">**AuthorizationFlags**</span><span class="sxs-lookup"><span data-stu-id="88f35-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-123">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ 旗標」 ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( 「印表機」、「通訊」、「伺服器」、「帳戶」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-124">一組旗標，指定使用者有權使用或修改的資源。</span><span class="sxs-lookup"><span data-stu-id="88f35-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="88f35-125">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="88f35-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-126">印表機</span><span class="sxs-lookup"><span data-stu-id="88f35-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="88f35-127">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="88f35-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-128">通訊</span><span class="sxs-lookup"><span data-stu-id="88f35-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="88f35-129">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="88f35-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-130">伺服器</span><span class="sxs-lookup"><span data-stu-id="88f35-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="88f35-131">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="88f35-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-132">帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88f35-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="88f35-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-136">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| NetUserEnum" ) </span><span class="sxs-lookup"><span data-stu-id="88f35-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-137">登入執行 Windows 的電腦系統時，使用者輸入錯誤密碼的次數。</span><span class="sxs-lookup"><span data-stu-id="88f35-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="88f35-138">範例：0</span><span class="sxs-lookup"><span data-stu-id="88f35-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="88f35-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="88f35-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-142">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="88f35-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88f35-143">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="88f35-143">Short textual description of the current object.</span></span>

<span data-ttu-id="88f35-144">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="88f35-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="88f35-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-148">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 代碼 \_ 頁」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-149">使用者選擇之語言的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="88f35-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="88f35-150">字碼頁是使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="88f35-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-151">**註解**</span><span class="sxs-lookup"><span data-stu-id="88f35-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-154">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 批註」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-155">此登入設定檔的批註或描述。</span><span class="sxs-lookup"><span data-stu-id="88f35-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="88f35-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-159">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ country \_ code」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-160">使用者選擇之語言的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="88f35-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="88f35-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88f35-164">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="88f35-164">Textual description of the current object.</span></span>

<span data-ttu-id="88f35-165">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="88f35-166">**旗標**</span><span class="sxs-lookup"><span data-stu-id="88f35-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-169">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 旗標」 ) ， [**BitMap**](../wmisdk/standard-qualifiers.md) ( "0"，"1"、"3"、"4"、"5"、"6"、"7"、"8"、"9"、"11"、"12"、"13"、"16"、"17"、"18"、"19"、"20"、"21"、"22"、"23" ) ， [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Script"，"帳戶已停用"，"Home Dir Required"，"鎖定"，"不需要密碼"，"Paswword"，"無法變更"，「允許的加密測試密碼」，"Temp 重複的帳戶"，"Normal account"，"域信任帳戶"、「工作站信任帳戶」、「伺服器信任帳戶」、「不要過期密碼」、「MNS 登入帳戶」、「需要智慧卡」、「受信任的委派」、「未委派」、「僅使用 DES 金鑰」、「不需要 Preauthorization」、「密碼已過期」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-170">此網路設定檔可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="88f35-170">The properties available to this network profile.</span></span>

<span data-ttu-id="88f35-171">可以設定的屬性包括：</span><span class="sxs-lookup"><span data-stu-id="88f35-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="88f35-172">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="88f35-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-173">指令碼</span><span class="sxs-lookup"><span data-stu-id="88f35-173">Script</span></span>

<span data-ttu-id="88f35-174">執行的登入腳本。</span><span class="sxs-lookup"><span data-stu-id="88f35-174">A logon script executed.</span></span> <span data-ttu-id="88f35-175">必須為 LAN Manager 2.0 設定這個值。</span><span class="sxs-lookup"><span data-stu-id="88f35-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-176">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="88f35-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-177">帳戶已停用</span><span class="sxs-lookup"><span data-stu-id="88f35-177">Account Disabled</span></span>

<span data-ttu-id="88f35-178">使用者的帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="88f35-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-179">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="88f35-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-180">需要主目錄</span><span class="sxs-lookup"><span data-stu-id="88f35-180">Home Directory Required</span></span>

<span data-ttu-id="88f35-181">需要主目錄。</span><span class="sxs-lookup"><span data-stu-id="88f35-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-182">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="88f35-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-183">鎖定</span><span class="sxs-lookup"><span data-stu-id="88f35-183">Lockout</span></span>

<span data-ttu-id="88f35-184">帳戶目前已鎖定。若為 [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)，可以清除此值以解除鎖定先前鎖定的帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="88f35-185">此值不能用來鎖定先前已解除鎖定的帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-186">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="88f35-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-187">不需要密碼</span><span class="sxs-lookup"><span data-stu-id="88f35-187">Password Not Required</span></span>

<span data-ttu-id="88f35-188">不需要密碼。</span><span class="sxs-lookup"><span data-stu-id="88f35-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-189">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="88f35-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-190">密碼無法變更</span><span class="sxs-lookup"><span data-stu-id="88f35-190">Password Cannot Change</span></span>

<span data-ttu-id="88f35-191">使用者無法變更密碼。</span><span class="sxs-lookup"><span data-stu-id="88f35-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-192">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="88f35-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-193">允許加密的測試密碼</span><span class="sxs-lookup"><span data-stu-id="88f35-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="88f35-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="88f35-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-195">暫存重複帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-195">Temp Duplicate Account</span></span>

<span data-ttu-id="88f35-196">其主要帳戶位於另一個網域的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="88f35-197">此帳戶可讓使用者存取此網域，但不提供任何信任此網域的網域。</span><span class="sxs-lookup"><span data-stu-id="88f35-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="88f35-198">使用者管理員會將此帳戶類型稱為本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-199">512 (0x200) </span><span class="sxs-lookup"><span data-stu-id="88f35-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-200">一般帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-200">Normal Account</span></span>

<span data-ttu-id="88f35-201">代表一般使用者的預設帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="88f35-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-202">2048 (0x800) </span><span class="sxs-lookup"><span data-stu-id="88f35-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-203">限域信任帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-203">Interdomain Trust Account</span></span>

<span data-ttu-id="88f35-204">針對信任其他網域的網域允許信任帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-205">4096 (0x1000) </span><span class="sxs-lookup"><span data-stu-id="88f35-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-206">工作站信任帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-206">Workstation Trust Account</span></span>

<span data-ttu-id="88f35-207">屬於此網域成員的 Windows 工作站或伺服器的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-208">8192 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="88f35-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-209">伺服器信任帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-209">Server Trust Account</span></span>

<span data-ttu-id="88f35-210">屬於此網域成員的備份網域控制站的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-211">65536 (0x10000) </span><span class="sxs-lookup"><span data-stu-id="88f35-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-212">不要過期密碼</span><span class="sxs-lookup"><span data-stu-id="88f35-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="88f35-213">131072 (0x20000) </span><span class="sxs-lookup"><span data-stu-id="88f35-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-214">MNS 登入帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-214">MNS Logon Account</span></span>

<span data-ttu-id="88f35-215">多數節點集 (MNS) 登入帳戶類型，代表一則 MNS 使用者。</span><span class="sxs-lookup"><span data-stu-id="88f35-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-216">262144 (0x40000) </span><span class="sxs-lookup"><span data-stu-id="88f35-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-217">需要智慧卡</span><span class="sxs-lookup"><span data-stu-id="88f35-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="88f35-218">524288 (0x80000) </span><span class="sxs-lookup"><span data-stu-id="88f35-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-219">受信任以進行委派</span><span class="sxs-lookup"><span data-stu-id="88f35-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="88f35-220">1048576 (0x100000) </span><span class="sxs-lookup"><span data-stu-id="88f35-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-221">未委派</span><span class="sxs-lookup"><span data-stu-id="88f35-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="88f35-222">2097152 (0x200000) </span><span class="sxs-lookup"><span data-stu-id="88f35-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-223">僅使用 DES 金鑰</span><span class="sxs-lookup"><span data-stu-id="88f35-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="88f35-224">4194304 (0x400000) </span><span class="sxs-lookup"><span data-stu-id="88f35-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-225">不需要 Preauthorization</span><span class="sxs-lookup"><span data-stu-id="88f35-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="88f35-226">8388608 (0x800000) </span><span class="sxs-lookup"><span data-stu-id="88f35-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="88f35-227">密碼已過期</span><span class="sxs-lookup"><span data-stu-id="88f35-227">Password Expired</span></span>

<span data-ttu-id="88f35-228">指出密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="88f35-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="88f35-229">下列屬性描述帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="88f35-229">The following properties describe the account type.</span></span> <span data-ttu-id="88f35-230">只能設定一個值：</span><span class="sxs-lookup"><span data-stu-id="88f35-230">Only one value can be set:</span></span>

-   <span data-ttu-id="88f35-231">UF \_ 一般 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="88f35-232">UF \_ 暫存 \_ 重複 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="88f35-233">UF \_ 工作站 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="88f35-234">UF \_ 伺服器 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="88f35-235">每個 UF \_ 域 \_ 信任 \_ 帳戶</span><span class="sxs-lookup"><span data-stu-id="88f35-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="88f35-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="88f35-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-239">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ full \_ name" ) </span><span class="sxs-lookup"><span data-stu-id="88f35-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-240">屬於網路登入設定檔之使用者的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="88f35-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="88f35-241">如果使用者選擇不將完整名稱與使用者名稱建立關聯，這個字串可以是空的。</span><span class="sxs-lookup"><span data-stu-id="88f35-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="88f35-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-245">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-246">使用者主目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="88f35-246">Path to the home directory of the user.</span></span> <span data-ttu-id="88f35-247">如果使用者選擇不指定主目錄，此字串可能是空的。</span><span class="sxs-lookup"><span data-stu-id="88f35-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="88f35-248">範例： " \\ HOMEDIR"</span><span class="sxs-lookup"><span data-stu-id="88f35-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-249">**HomeDirectoryDrive**</span><span class="sxs-lookup"><span data-stu-id="88f35-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-252">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir \_ 磁片磁碟機」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-253">指派給使用者的主目錄以供登入之用的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="88f35-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="88f35-254">範例： "C："</span><span class="sxs-lookup"><span data-stu-id="88f35-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-255">**LastLogoff**</span><span class="sxs-lookup"><span data-stu-id="88f35-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-256">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88f35-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-258">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 上次 \_ 登出」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-259">使用者上次登出系統。</span><span class="sxs-lookup"><span data-stu-id="88f35-259">User last logged off the system.</span></span> <span data-ttu-id="88f35-260">此值的計算是00:00:00 自1970年1月1日起經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="88f35-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="88f35-261">值為 " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " 表示最後一次登出時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="88f35-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="88f35-262">此值的格式為 yyyymmddhhmmss.ffffff. mmmmmm sutc。</span><span class="sxs-lookup"><span data-stu-id="88f35-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="88f35-263">如需將此屬性轉譯為本地時間的詳細資訊，請參閱 [WMI 工作：日期和時間](../wmisdk/wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="88f35-264">範例： 19521201000230.000000 000</span><span class="sxs-lookup"><span data-stu-id="88f35-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="88f35-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="88f35-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-266">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88f35-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-268">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 上次 \_ 登入」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-269">使用者上次登入系統的時間。</span><span class="sxs-lookup"><span data-stu-id="88f35-269">User last logged on to the system.</span></span> <span data-ttu-id="88f35-270">此值的計算是00:00:00 自1970年1月1日起經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="88f35-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="88f35-271">此值的格式為 yyyymmddhhmmss.ffffff. mmmmmm sutc。</span><span class="sxs-lookup"><span data-stu-id="88f35-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="88f35-272">如需將此屬性轉譯為本地時間的詳細資訊，請參閱 [WMI 工作：日期和時間](../wmisdk/wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="88f35-273">範例： 19521201000230.000000 000</span><span class="sxs-lookup"><span data-stu-id="88f35-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="88f35-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="88f35-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-277">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (147) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 登入時數」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="88f35-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-278">使用者可以登入的時間。</span><span class="sxs-lookup"><span data-stu-id="88f35-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="88f35-279">每個位代表 **UnitsPerWeek** 屬性指定的時間單位。</span><span class="sxs-lookup"><span data-stu-id="88f35-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="88f35-280">比方說，如果時間單位是每小時，第一個位 (位0，word 0) 是星期日、0:00 到0:59、第二個位 (bit 1、word 0) 是星期日、1:00 至1:59 等等。</span><span class="sxs-lookup"><span data-stu-id="88f35-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="88f35-281">如果這個成員設定為 **Null**，則沒有時間限制。</span><span class="sxs-lookup"><span data-stu-id="88f35-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="88f35-282">時間會設定為 GMT，且必須針對其他時區進行調整 (例如，在 PST) 的 GMT 減去8小時。</span><span class="sxs-lookup"><span data-stu-id="88f35-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="88f35-283">**LogonServer**</span><span class="sxs-lookup"><span data-stu-id="88f35-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-286">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 登入 \_ 伺服器」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-287">傳送登入要求的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="88f35-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="88f35-288">伺服器名稱的前面應該要有兩個反斜線 (\\ \\) 。</span><span class="sxs-lookup"><span data-stu-id="88f35-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="88f35-289">具有星號 (的伺服器名稱 \\ \\ \*) 表示登入要求可以由任何登入伺服器處理。</span><span class="sxs-lookup"><span data-stu-id="88f35-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="88f35-290">Null 字串表示將要求傳送至網域控制站。</span><span class="sxs-lookup"><span data-stu-id="88f35-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="88f35-291">範例： " \\ \\ MyServer"</span><span class="sxs-lookup"><span data-stu-id="88f35-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="88f35-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-293">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88f35-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-295">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 儲存體上限」 \_ ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-296">可供使用者使用的最大磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="88f35-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="88f35-297">如果 MaximumStorage 設定為 \_ \_ [無限制使用者 MAXSTORAGE]，則允許使用者使用所有可用的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="88f35-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="88f35-298">範例：10000000</span><span class="sxs-lookup"><span data-stu-id="88f35-298">Example: 10000000</span></span>

<span data-ttu-id="88f35-299">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="88f35-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88f35-300">**名稱**</span><span class="sxs-lookup"><span data-stu-id="88f35-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-303">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ name" ) </span><span class="sxs-lookup"><span data-stu-id="88f35-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-304">特定網域或電腦上的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="88f35-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="88f35-305">名稱中的字元數不能超過 UNLEN 的值。</span><span class="sxs-lookup"><span data-stu-id="88f35-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="88f35-306">範例： "n \\ johndoe"</span><span class="sxs-lookup"><span data-stu-id="88f35-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-307">**NumberOfLogons**</span><span class="sxs-lookup"><span data-stu-id="88f35-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-308">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-310">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num 登入」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="88f35-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-311">使用者嘗試登入此帳戶的成功次數。</span><span class="sxs-lookup"><span data-stu-id="88f35-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="88f35-312">0xFFFFFFFF 的值表示值不明。</span><span class="sxs-lookup"><span data-stu-id="88f35-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="88f35-313">這個屬性會在網域中 (BDC) 的每個備份網域控制站上分開維護。</span><span class="sxs-lookup"><span data-stu-id="88f35-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="88f35-314">若要取得精確的值，應該只使用來自所有 Bdc 的最大值。</span><span class="sxs-lookup"><span data-stu-id="88f35-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="88f35-315">範例: 4</span><span class="sxs-lookup"><span data-stu-id="88f35-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="88f35-316">**參數**</span><span class="sxs-lookup"><span data-stu-id="88f35-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-319">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-320">留有空間供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="88f35-320">Space set aside for use by applications.</span></span> <span data-ttu-id="88f35-321">這個字串可以是 null，也可以在終止的 null 字元之前有任意數目的字元。</span><span class="sxs-lookup"><span data-stu-id="88f35-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="88f35-322">Microsoft 產品會使用這個成員來儲存使用者設定資訊。</span><span class="sxs-lookup"><span data-stu-id="88f35-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="88f35-323">請勿修改此資訊，因為此值是應用程式特有的。</span><span class="sxs-lookup"><span data-stu-id="88f35-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-324">**PasswordAge**</span><span class="sxs-lookup"><span data-stu-id="88f35-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-325">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88f35-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-327">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 密碼 \_ 使用期限」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-328">密碼生效的時間長度。</span><span class="sxs-lookup"><span data-stu-id="88f35-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="88f35-329">此值是從上次變更密碼以來經過的秒數來測量。</span><span class="sxs-lookup"><span data-stu-id="88f35-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="88f35-330">範例： 00001201000230.000000 000</span><span class="sxs-lookup"><span data-stu-id="88f35-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="88f35-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="88f35-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-332">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88f35-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-334">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ MODALS \_ 資訊 \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ 最大 \_ 密碼 \_ 存留期」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-335">密碼過期的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="88f35-335">Date and time the password expires.</span></span> <span data-ttu-id="88f35-336">此值的設定格式如下： yyyymmddhhmmss.ffffff. mmmmmm sutc</span><span class="sxs-lookup"><span data-stu-id="88f35-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="88f35-337">範例： 19521201000230.000000 000</span><span class="sxs-lookup"><span data-stu-id="88f35-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="88f35-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="88f35-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-339">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-341">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 主要 \_ 群組 \_ 識別碼」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-342">此使用者的主要全域群組 (RID) 的相對識別碼。</span><span class="sxs-lookup"><span data-stu-id="88f35-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="88f35-343">此識別碼會驗證使用者設定檔所屬的主要群組。</span><span class="sxs-lookup"><span data-stu-id="88f35-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-344">**特權**</span><span class="sxs-lookup"><span data-stu-id="88f35-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-345">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-347">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 的特權」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="88f35-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-348">指派給 **usri3 \_ name** 屬性的許可權層級。</span><span class="sxs-lookup"><span data-stu-id="88f35-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="88f35-349">**來賓** (0) </span><span class="sxs-lookup"><span data-stu-id="88f35-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="88f35-350">**使用者** (1) </span><span class="sxs-lookup"><span data-stu-id="88f35-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="88f35-351">**系統管理員** (2) </span><span class="sxs-lookup"><span data-stu-id="88f35-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88f35-352">**設定檔**</span><span class="sxs-lookup"><span data-stu-id="88f35-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-355">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 設定檔」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-356">使用者設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="88f35-356">Path to the user's profile.</span></span> <span data-ttu-id="88f35-357">這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="88f35-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="88f35-358">使用者設定檔包含可針對每個使用者自訂的設定，例如桌面色彩。</span><span class="sxs-lookup"><span data-stu-id="88f35-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="88f35-359">範例： "C： \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="88f35-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="88f35-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-363">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 腳本 \_ 路徑」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-364">使用者登入腳本的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="88f35-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="88f35-365">登入腳本會在每次使用者登入系統時，自動執行一組命令。</span><span class="sxs-lookup"><span data-stu-id="88f35-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="88f35-366">範例： "C： \\ win \\ profiles \\ ThomasSteven"</span><span class="sxs-lookup"><span data-stu-id="88f35-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="88f35-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="88f35-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-368">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-370">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="88f35-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="88f35-371">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88f35-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="88f35-372">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="88f35-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="88f35-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-374">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-376">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ 每週的 usri3 單位」 \_ \_ ) </span><span class="sxs-lookup"><span data-stu-id="88f35-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-377">一周所分割的時間單位數。</span><span class="sxs-lookup"><span data-stu-id="88f35-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="88f35-378">它會搭配 **LogonHours** 屬性使用，以限制使用者對電腦的存取權。</span><span class="sxs-lookup"><span data-stu-id="88f35-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="88f35-379">範例：每週 168 (小時) </span><span class="sxs-lookup"><span data-stu-id="88f35-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="88f35-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="88f35-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-383">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ 批註」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-384">此設定檔的使用者定義批註或描述。</span><span class="sxs-lookup"><span data-stu-id="88f35-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="88f35-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-386">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88f35-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-388">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 使用者 \_ 識別碼」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-389">使用者的 RID。</span><span class="sxs-lookup"><span data-stu-id="88f35-389">RID of the user.</span></span> <span data-ttu-id="88f35-390">此識別碼會驗證使用者是否存在，而且對此網域而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="88f35-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="88f35-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="88f35-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-394">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 旗標」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-395">使用者具有許可權的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="88f35-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="88f35-396">值如下：</span><span class="sxs-lookup"><span data-stu-id="88f35-396">The values are:</span></span>

-   <span data-ttu-id="88f35-397">「一般帳戶」</span><span class="sxs-lookup"><span data-stu-id="88f35-397">"Normal Account"</span></span>
-   <span data-ttu-id="88f35-398">「重複的帳戶」</span><span class="sxs-lookup"><span data-stu-id="88f35-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="88f35-399">「工作站信任帳戶」</span><span class="sxs-lookup"><span data-stu-id="88f35-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="88f35-400">「伺服器信任帳戶」</span><span class="sxs-lookup"><span data-stu-id="88f35-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="88f35-401">「限域信任帳戶」</span><span class="sxs-lookup"><span data-stu-id="88f35-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="88f35-402">不明</span><span class="sxs-lookup"><span data-stu-id="88f35-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="88f35-403">**一般帳戶** ( 「一般帳戶」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="88f35-404">**重複的帳戶** ( 「重複的帳戶」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="88f35-405">**工作站信任帳戶** ( 「工作站信任帳戶」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="88f35-406">**伺服器信任帳戶** ( [伺服器信任帳戶] ) </span><span class="sxs-lookup"><span data-stu-id="88f35-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="88f35-407">「域間信任帳戶 **」 ( 「域間信任帳戶**」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88f35-408">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88f35-409">**工作站**</span><span class="sxs-lookup"><span data-stu-id="88f35-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88f35-410">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88f35-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88f35-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88f35-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88f35-412">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 工作站」 ) </span><span class="sxs-lookup"><span data-stu-id="88f35-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="88f35-413">使用者可以登入的工作站名稱。</span><span class="sxs-lookup"><span data-stu-id="88f35-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="88f35-414">最多可指定八個工作站;這些名稱必須以逗號分隔 (，) 。</span><span class="sxs-lookup"><span data-stu-id="88f35-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="88f35-415">Null 字串表示沒有限制。</span><span class="sxs-lookup"><span data-stu-id="88f35-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="88f35-416">若要停用此帳戶的所有工作站登入，請 \_ 在此類別的 [ **旗標** ] 屬性中設定 [UF] ACCOUNTDISABLE。</span><span class="sxs-lookup"><span data-stu-id="88f35-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88f35-417">備註</span><span class="sxs-lookup"><span data-stu-id="88f35-417">Remarks</span></span>

<span data-ttu-id="88f35-418">**Win32 \_ NetworkLoginProfile** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="88f35-419">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="88f35-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="88f35-420">如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="88f35-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88f35-421">範例</span><span class="sxs-lookup"><span data-stu-id="88f35-421">Examples</span></span>

<span data-ttu-id="88f35-422">[列出網路登入設定檔](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14)PowerShell 範例會傳回電腦上所有使用者的網路登入資訊。</span><span class="sxs-lookup"><span data-stu-id="88f35-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="88f35-423">下列 VBScript 範例會傳回網路登入資訊。</span><span class="sxs-lookup"><span data-stu-id="88f35-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="88f35-424">規格需求</span><span class="sxs-lookup"><span data-stu-id="88f35-424">Requirements</span></span>



| <span data-ttu-id="88f35-425">需求</span><span class="sxs-lookup"><span data-stu-id="88f35-425">Requirement</span></span> | <span data-ttu-id="88f35-426">值</span><span class="sxs-lookup"><span data-stu-id="88f35-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f35-427">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88f35-427">Minimum supported client</span></span><br/> | <span data-ttu-id="88f35-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88f35-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88f35-429">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88f35-429">Minimum supported server</span></span><br/> | <span data-ttu-id="88f35-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88f35-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88f35-431">命名空間</span><span class="sxs-lookup"><span data-stu-id="88f35-431">Namespace</span></span><br/>                | <span data-ttu-id="88f35-432">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88f35-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88f35-433">MOF</span><span class="sxs-lookup"><span data-stu-id="88f35-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88f35-434"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="88f35-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88f35-435">DLL</span><span class="sxs-lookup"><span data-stu-id="88f35-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88f35-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f35-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f35-437">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88f35-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f35-438">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="88f35-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="88f35-439">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="88f35-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
