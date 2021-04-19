---
description: Win32 \_ DCOMApplicationSetting&\# 8194;WMI 類別代表 DCOM 應用程式的設定。
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973184"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="f45cb-103">Win32 \_ DCOMApplicationSetting 類別</span><span class="sxs-lookup"><span data-stu-id="f45cb-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="f45cb-104">**Win32 \_ DCOMApplicationSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 DCOM 應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="f45cb-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="f45cb-105">它包含與登錄中的 **AppID** 金鑰相關聯的 DCOM 設定選項。</span><span class="sxs-lookup"><span data-stu-id="f45cb-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="f45cb-106">這些選項在以邏輯方式分組于指定應用程式類別之下的元件上是有效的。</span><span class="sxs-lookup"><span data-stu-id="f45cb-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="f45cb-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f45cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f45cb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f45cb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f45cb-109">語法</span><span class="sxs-lookup"><span data-stu-id="f45cb-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="f45cb-110">成員</span><span class="sxs-lookup"><span data-stu-id="f45cb-110">Members</span></span>

<span data-ttu-id="f45cb-111">**Win32 \_ DCOMApplicationSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f45cb-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f45cb-112">方法</span><span class="sxs-lookup"><span data-stu-id="f45cb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f45cb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f45cb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f45cb-114">方法</span><span class="sxs-lookup"><span data-stu-id="f45cb-114">Methods</span></span>

<span data-ttu-id="f45cb-115">**Win32 \_ DCOMApplicationSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f45cb-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="f45cb-116">方法</span><span class="sxs-lookup"><span data-stu-id="f45cb-116">Method</span></span>                                                                                                                        | <span data-ttu-id="f45cb-117">描述</span><span class="sxs-lookup"><span data-stu-id="f45cb-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f45cb-118">**GetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f45cb-119">取得安全描述項，以控制允許存取 DCOM 應用程式的人員。</span><span class="sxs-lookup"><span data-stu-id="f45cb-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f45cb-120">**GetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="f45cb-121">取得安全描述項，以控制允許哪些人設定 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f45cb-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f45cb-122">**GetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="f45cb-123">取得安全描述項，可控制哪些人可以啟動 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f45cb-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f45cb-124">**SetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f45cb-125">使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的存取安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f45cb-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="f45cb-126">**SetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="f45cb-127">使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的設定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f45cb-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="f45cb-128">**SetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f45cb-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f45cb-129">使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的啟動安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f45cb-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="f45cb-130">屬性</span><span class="sxs-lookup"><span data-stu-id="f45cb-130">Properties</span></span>

<span data-ttu-id="f45cb-131">**Win32 \_ DCOMApplicationSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f45cb-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f45cb-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="f45cb-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-135">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-136">這個 DCOM 應用程式的全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="f45cb-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="f45cb-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f45cb-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f45cb-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-140">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-141">此 COM 伺服器所需的最小用戶端驗證等級。</span><span class="sxs-lookup"><span data-stu-id="f45cb-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="f45cb-142">如果是 **Null**，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="f45cb-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="f45cb-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (1) </span><span class="sxs-lookup"><span data-stu-id="f45cb-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-144">無 (不執行任何驗證) </span><span class="sxs-lookup"><span data-stu-id="f45cb-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="f45cb-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**連接** (2) </span><span class="sxs-lookup"><span data-stu-id="f45cb-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-146">只有當用戶端與應用程式建立關聯性時，才會執行 Connect (驗證) </span><span class="sxs-lookup"><span data-stu-id="f45cb-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="f45cb-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**呼叫** (3) </span><span class="sxs-lookup"><span data-stu-id="f45cb-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-148">只有當應用程式收到要求時，才會在每次呼叫開始時執行呼叫 (驗證) </span><span class="sxs-lookup"><span data-stu-id="f45cb-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="f45cb-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>封 **包** (4) </span><span class="sxs-lookup"><span data-stu-id="f45cb-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-150">封包 (驗證是在從用戶端接收的所有資料上執行) </span><span class="sxs-lookup"><span data-stu-id="f45cb-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="f45cb-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5) </span><span class="sxs-lookup"><span data-stu-id="f45cb-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-152">PacketIntegrity (在用戶端和應用程式之間傳送的所有資料都會經過驗證和驗證) </span><span class="sxs-lookup"><span data-stu-id="f45cb-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="f45cb-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6) </span><span class="sxs-lookup"><span data-stu-id="f45cb-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f45cb-154">PacketPrivacy (會使用其他驗證等級的屬性，並加密所有資料) </span><span class="sxs-lookup"><span data-stu-id="f45cb-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f45cb-155">**標題**</span><span class="sxs-lookup"><span data-stu-id="f45cb-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-158">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f45cb-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-159">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="f45cb-159">Short textual description of the current object.</span></span>

<span data-ttu-id="f45cb-160">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="f45cb-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-161">**CustomSurrogate**</span><span class="sxs-lookup"><span data-stu-id="f45cb-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-165">啟用內含式 DCOM 應用程式之自訂代理的名稱。</span><span class="sxs-lookup"><span data-stu-id="f45cb-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="f45cb-166">如果這個值是 **Null** ，且 **UseSurrogate** 索引鍵為 **TRUE**，則系統會提供代理程式。</span><span class="sxs-lookup"><span data-stu-id="f45cb-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-167">**說明**</span><span class="sxs-lookup"><span data-stu-id="f45cb-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-170">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f45cb-170">Textual description of the current object.</span></span>

<span data-ttu-id="f45cb-171">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="f45cb-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="f45cb-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-173">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f45cb-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-175">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-176">DCOM 應用程式會從第一次初始化應用程式的狀態，抓取應用程式的儲存狀態或開始。</span><span class="sxs-lookup"><span data-stu-id="f45cb-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-177">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="f45cb-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-180">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-181">DCOM 應用程式所提供之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f45cb-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="f45cb-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f45cb-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-185">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-186">啟用應用程式的遠端伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f45cb-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="f45cb-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-190">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RunAs \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-191">要在啟用時執行應用程式的特定使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="f45cb-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-192">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="f45cb-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-195">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-196">傳遞至 DCOM 應用程式的命令列參數。</span><span class="sxs-lookup"><span data-stu-id="f45cb-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="f45cb-197">只有當應用程式是以 Windows 為基礎的服務撰寫時，才會有效。</span><span class="sxs-lookup"><span data-stu-id="f45cb-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="f45cb-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f45cb-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f45cb-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-201">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="f45cb-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-202">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f45cb-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="f45cb-203">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="f45cb-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f45cb-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="f45cb-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f45cb-205">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f45cb-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-206">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f45cb-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f45cb-207">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] " ) </span><span class="sxs-lookup"><span data-stu-id="f45cb-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="f45cb-208">您可以使用代理可執行檔，將 DCOM 應用程式啟用為跨進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="f45cb-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f45cb-209">備註</span><span class="sxs-lookup"><span data-stu-id="f45cb-209">Remarks</span></span>

<span data-ttu-id="f45cb-210">**Win32 \_ DCOMApplicationSetting** 類別衍生自 [**win32 \_ COMSetting**](win32-comsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="f45cb-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f45cb-211">規格需求</span><span class="sxs-lookup"><span data-stu-id="f45cb-211">Requirements</span></span>



| <span data-ttu-id="f45cb-212">需求</span><span class="sxs-lookup"><span data-stu-id="f45cb-212">Requirement</span></span> | <span data-ttu-id="f45cb-213">值</span><span class="sxs-lookup"><span data-stu-id="f45cb-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f45cb-214">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f45cb-214">Minimum supported client</span></span><br/> | <span data-ttu-id="f45cb-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f45cb-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f45cb-216">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f45cb-216">Minimum supported server</span></span><br/> | <span data-ttu-id="f45cb-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f45cb-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f45cb-218">命名空間</span><span class="sxs-lookup"><span data-stu-id="f45cb-218">Namespace</span></span><br/>                | <span data-ttu-id="f45cb-219">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f45cb-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f45cb-220">MOF</span><span class="sxs-lookup"><span data-stu-id="f45cb-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f45cb-221"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f45cb-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f45cb-222">DLL</span><span class="sxs-lookup"><span data-stu-id="f45cb-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f45cb-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f45cb-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f45cb-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f45cb-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f45cb-225">**Win32 \_ COMSetting**</span><span class="sxs-lookup"><span data-stu-id="f45cb-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="f45cb-226">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f45cb-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f45cb-227">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="f45cb-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="f45cb-228">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="f45cb-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="f45cb-229">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="f45cb-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

