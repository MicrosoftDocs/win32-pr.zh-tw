---
title: Win32_TSLogonSetting 類別
description: 定義與 \_ 用戶端登入相關的 Win32 終端機類別的配置設定。
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting 類別遠端桌面服務
- Win32_TSLogonSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384957"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="ea4e7-105">Win32 \_ TSLogonSetting 類別</span><span class="sxs-lookup"><span data-stu-id="ea4e7-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="ea4e7-106">**Win32 \_ TSLogonSetting** WMI 類別會定義與用戶端登入相關的 [**win32 \_ 終端**](win32-terminal.md)機類別的設定。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="ea4e7-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="ea4e7-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4e7-109">語法</span><span class="sxs-lookup"><span data-stu-id="ea4e7-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="ea4e7-110">成員</span><span class="sxs-lookup"><span data-stu-id="ea4e7-110">Members</span></span>

<span data-ttu-id="ea4e7-111">**Win32 \_ TSLogonSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea4e7-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ea4e7-112">方法</span><span class="sxs-lookup"><span data-stu-id="ea4e7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea4e7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ea4e7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea4e7-114">方法</span><span class="sxs-lookup"><span data-stu-id="ea4e7-114">Methods</span></span>

<span data-ttu-id="ea4e7-115">**Win32 \_ TSLogonSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="ea4e7-116">方法</span><span class="sxs-lookup"><span data-stu-id="ea4e7-116">Method</span></span>                                                                    | <span data-ttu-id="ea4e7-117">描述</span><span class="sxs-lookup"><span data-stu-id="ea4e7-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ea4e7-118">**ExplicitLogon**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="ea4e7-119">設定使用者名稱、密碼和網域驗證認證。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="ea4e7-120">**SetPromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="ea4e7-121">設定 **PromptForPassword** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="ea4e7-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ea4e7-122">Properties</span></span>

<span data-ttu-id="ea4e7-123">**Win32 \_ TSLogonSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea4e7-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-128">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ea4e7-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea4e7-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-133">伺服器用來判斷連接設定的原則。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="ea4e7-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ea4e7-135">個別使用者連接設定有效。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="ea4e7-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ea4e7-137">伺服器會覆寫個別使用者連接設定。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-141">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-141">Description of the object.</span></span>

<span data-ttu-id="ea4e7-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-143">**網域**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-146">使用者的網域登入驗證認證。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="ea4e7-147">這是使用者電腦所在的網域。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="ea4e7-148">這個屬性的長度不能超過17個字元。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-150">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-152">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="ea4e7-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-153">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-153">The date the object was installed.</span></span> <span data-ttu-id="ea4e7-154">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ea4e7-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-156">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-159">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-159">The name of the object.</span></span>

<span data-ttu-id="ea4e7-160">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-161">**密碼**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-164">使用者的密碼登入驗證認證。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="ea4e7-165">這個屬性的長度不能超過14個字元。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="ea4e7-166">如果您查詢此屬性，建議您將安全性層級設定為封包隱私權 (wbemAuthenticationLevelPktPrivacy = 6) 。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="ea4e7-167">這是因為不會在網路上加密密碼，而沒有此安全性層級。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="ea4e7-168">如需設定安全性層級的詳細資訊，請參閱 WMI SDK 檔中的 [設定用戶端應用程式安全性](/windows/desktop/WmiSdk/setting-client-application-process-security) 。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-169">**PolicySourceDomain**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-172">指出 **網域** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ea4e7-173">0</span><span class="sxs-lookup"><span data-stu-id="ea4e7-173">0</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-174">伺服器</span><span class="sxs-lookup"><span data-stu-id="ea4e7-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-175">1</span><span class="sxs-lookup"><span data-stu-id="ea4e7-175">1</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-176">群組原則</span><span class="sxs-lookup"><span data-stu-id="ea4e7-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-177">2</span><span class="sxs-lookup"><span data-stu-id="ea4e7-177">2</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-178">預設</span><span class="sxs-lookup"><span data-stu-id="ea4e7-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-180">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-182">指出 **PromptForPassword** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ea4e7-183">0</span><span class="sxs-lookup"><span data-stu-id="ea4e7-183">0</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-184">伺服器</span><span class="sxs-lookup"><span data-stu-id="ea4e7-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-185">1</span><span class="sxs-lookup"><span data-stu-id="ea4e7-185">1</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-186">群組原則</span><span class="sxs-lookup"><span data-stu-id="ea4e7-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-187">2</span><span class="sxs-lookup"><span data-stu-id="ea4e7-187">2</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-188">預設</span><span class="sxs-lookup"><span data-stu-id="ea4e7-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-189">**PolicySourceUserName**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-190">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-192">指出使用者 **名稱** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ea4e7-193">0</span><span class="sxs-lookup"><span data-stu-id="ea4e7-193">0</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-194">伺服器</span><span class="sxs-lookup"><span data-stu-id="ea4e7-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-195">1</span><span class="sxs-lookup"><span data-stu-id="ea4e7-195">1</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-196">群組原則</span><span class="sxs-lookup"><span data-stu-id="ea4e7-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-197">2</span><span class="sxs-lookup"><span data-stu-id="ea4e7-197">2</span></span>
</dt> <dd>

<span data-ttu-id="ea4e7-198">預設</span><span class="sxs-lookup"><span data-stu-id="ea4e7-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-200">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-202">指定在登入伺服器時，是否一律提示使用者輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ea4e7-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ea4e7-204">系統不會提示使用者輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ea4e7-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ea4e7-206">使用者會被提示輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-207">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-210">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-211">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-211">Current status of the object.</span></span> <span data-ttu-id="ea4e7-212">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ea4e7-213">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ea4e7-214">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ea4e7-215">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ea4e7-216">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ea4e7-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ea4e7-218"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-219"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-220"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-221"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-222"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-223"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-224"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ea4e7-225"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="ea4e7-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea4e7-226">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-229">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-229">The name of the terminal.</span></span>

<span data-ttu-id="ea4e7-230">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea4e7-231">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4e7-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4e7-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4e7-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4e7-234">使用者的使用者名稱登入驗證認證。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="ea4e7-235">這個屬性的長度不能超過20個字元。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea4e7-236">備註</span><span class="sxs-lookup"><span data-stu-id="ea4e7-236">Remarks</span></span>

<span data-ttu-id="ea4e7-237">請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="ea4e7-238">如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="ea4e7-239">如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，則會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="ea4e7-240">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ea4e7-241">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ea4e7-242">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ea4e7-243">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ea4e7-244">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ea4e7-245">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ea4e7-246">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ea4e7-247">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="ea4e7-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4e7-248">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea4e7-248">Requirements</span></span>



| <span data-ttu-id="ea4e7-249">需求</span><span class="sxs-lookup"><span data-stu-id="ea4e7-249">Requirement</span></span> | <span data-ttu-id="ea4e7-250">值</span><span class="sxs-lookup"><span data-stu-id="ea4e7-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4e7-251">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea4e7-251">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4e7-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea4e7-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea4e7-253">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea4e7-253">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4e7-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea4e7-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea4e7-255">命名空間</span><span class="sxs-lookup"><span data-stu-id="ea4e7-255">Namespace</span></span><br/>                | <span data-ttu-id="ea4e7-256">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ea4e7-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ea4e7-257">MOF</span><span class="sxs-lookup"><span data-stu-id="ea4e7-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea4e7-258"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e7-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea4e7-259">DLL</span><span class="sxs-lookup"><span data-stu-id="ea4e7-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4e7-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e7-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4e7-261">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea4e7-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4e7-262">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="ea4e7-263">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="ea4e7-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

