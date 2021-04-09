---
description: 描述與登入執行 Windows 的電腦系統之使用者相關聯的登入會話或會話。
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Win32_LogonSession 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688668"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="84a63-103">Win32 \_ LogonSession 類別</span><span class="sxs-lookup"><span data-stu-id="84a63-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="84a63-104">**Win32 \_ LogonSession** wmi 類別 (請參閱) 說明如何抓取 [wmi 類別](/windows/desktop/wmisdk/retrieving-a-class)，以描述與登入執行 Windows 之電腦系統的使用者相關聯的登入會話或會話。</span><span class="sxs-lookup"><span data-stu-id="84a63-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="84a63-105">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a63-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="84a63-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="84a63-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a63-107">語法</span><span class="sxs-lookup"><span data-stu-id="84a63-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="84a63-108">成員</span><span class="sxs-lookup"><span data-stu-id="84a63-108">Members</span></span>

<span data-ttu-id="84a63-109">**Win32 \_ LogonSession** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84a63-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="84a63-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84a63-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84a63-111">屬性</span><span class="sxs-lookup"><span data-stu-id="84a63-111">Properties</span></span>

<span data-ttu-id="84a63-112">**Win32 \_ LogonSession** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84a63-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84a63-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="84a63-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84a63-116">用來驗證登入會話的子系統名稱。</span><span class="sxs-lookup"><span data-stu-id="84a63-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="84a63-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="84a63-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="84a63-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84a63-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="84a63-121">A short textual description of the object.</span></span>

<span data-ttu-id="84a63-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84a63-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="84a63-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-126">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="84a63-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84a63-127">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="84a63-127">A textual description of the object.</span></span>

<span data-ttu-id="84a63-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84a63-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84a63-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-130">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="84a63-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="84a63-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84a63-133">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="84a63-133">Indicates when the object was installed.</span></span> <span data-ttu-id="84a63-134">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="84a63-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="84a63-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84a63-136">**LogonId**</span><span class="sxs-lookup"><span data-stu-id="84a63-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84a63-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84a63-140">指派給登入會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="84a63-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="84a63-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="84a63-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84a63-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84a63-144">指出登入會話類型的數值。</span><span class="sxs-lookup"><span data-stu-id="84a63-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="84a63-145">0</span><span class="sxs-lookup"><span data-stu-id="84a63-145">0</span></span>
</dt> <dd>

<span data-ttu-id="84a63-146">只能由系統帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="84a63-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="84a63-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**互動式** (2) </span><span class="sxs-lookup"><span data-stu-id="84a63-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-148">適用于以互動方式使用電腦的使用者，例如由終端機伺服器登入的使用者、遠端 shell 或類似的進程。</span><span class="sxs-lookup"><span data-stu-id="84a63-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="84a63-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3) </span><span class="sxs-lookup"><span data-stu-id="84a63-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-150">適用于可驗證純文字密碼的高效能伺服器。</span><span class="sxs-lookup"><span data-stu-id="84a63-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="84a63-151">LogonUser 不會快取此登入類型的認證。</span><span class="sxs-lookup"><span data-stu-id="84a63-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="84a63-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4) </span><span class="sxs-lookup"><span data-stu-id="84a63-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-153">適用于批次伺服器，在此情況下可以代表使用者執行處理常式，而不需直接介入;或適用于一次處理許多純文字驗證嘗試的較高效能伺服器，例如郵件或網頁伺服器。</span><span class="sxs-lookup"><span data-stu-id="84a63-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="84a63-154">LogonUser 不會快取此登入類型的認證。</span><span class="sxs-lookup"><span data-stu-id="84a63-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84a63-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務** (5) </span><span class="sxs-lookup"><span data-stu-id="84a63-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-156">表示服務類型登入。</span><span class="sxs-lookup"><span data-stu-id="84a63-156">Indicates a service-type logon.</span></span> <span data-ttu-id="84a63-157">提供的帳戶必須啟用服務許可權。</span><span class="sxs-lookup"><span data-stu-id="84a63-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="84a63-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6) </span><span class="sxs-lookup"><span data-stu-id="84a63-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-159">表示 proxy 型別登入。</span><span class="sxs-lookup"><span data-stu-id="84a63-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="84a63-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span> (7) **解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="84a63-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-161">這種登入類型適用于以互動方式使用電腦之使用者的 GINA Dll 記錄。</span><span class="sxs-lookup"><span data-stu-id="84a63-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="84a63-162">此登入類型允許產生唯一的審核記錄，以顯示工作站解除鎖定的時間。</span><span class="sxs-lookup"><span data-stu-id="84a63-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="84a63-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8) </span><span class="sxs-lookup"><span data-stu-id="84a63-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-164">會保留驗證套件中的名稱和密碼，讓伺服器可以在模擬用戶端時，連接到其他網路伺服器。</span><span class="sxs-lookup"><span data-stu-id="84a63-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="84a63-165">這可讓伺服器接受來自用戶端的純文字認證、呼叫 LogonUser、驗證使用者是否可透過網路存取系統，並仍與其他伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="84a63-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="84a63-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9) </span><span class="sxs-lookup"><span data-stu-id="84a63-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-167">允許呼叫者複製其目前的權杖，並指定輸出連接的新認證。</span><span class="sxs-lookup"><span data-stu-id="84a63-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="84a63-168">新的登入會話具有相同的本機識別，但是針對其他網路連線使用不同的認證。</span><span class="sxs-lookup"><span data-stu-id="84a63-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="84a63-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10) </span><span class="sxs-lookup"><span data-stu-id="84a63-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-170">同時為遠端和互動式的終端機服務會話。</span><span class="sxs-lookup"><span data-stu-id="84a63-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="84a63-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11) </span><span class="sxs-lookup"><span data-stu-id="84a63-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-172">嘗試快取的認證，而不需要存取網路。</span><span class="sxs-lookup"><span data-stu-id="84a63-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="84a63-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12) </span><span class="sxs-lookup"><span data-stu-id="84a63-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-174">與 RemoteInteractive 相同。</span><span class="sxs-lookup"><span data-stu-id="84a63-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="84a63-175">這可用於內部審核。</span><span class="sxs-lookup"><span data-stu-id="84a63-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="84a63-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13) </span><span class="sxs-lookup"><span data-stu-id="84a63-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="84a63-177">工作站登入。</span><span class="sxs-lookup"><span data-stu-id="84a63-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84a63-178">**名稱**</span><span class="sxs-lookup"><span data-stu-id="84a63-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-181">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="84a63-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="84a63-182">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="84a63-182">Label by which the object is known.</span></span> <span data-ttu-id="84a63-183">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="84a63-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="84a63-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84a63-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="84a63-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-186">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="84a63-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84a63-188">會話開始的時間。</span><span class="sxs-lookup"><span data-stu-id="84a63-188">Time at which the session started.</span></span>

<span data-ttu-id="84a63-189">這個屬性繼承自 [**Win32 \_ 會話**](win32-session.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="84a63-190">**狀態**</span><span class="sxs-lookup"><span data-stu-id="84a63-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84a63-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84a63-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84a63-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84a63-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84a63-193">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="84a63-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84a63-194">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="84a63-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="84a63-195">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="84a63-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="84a63-196">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="84a63-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="84a63-197">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="84a63-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="84a63-198">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="84a63-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="84a63-199">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="84a63-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="84a63-200">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="84a63-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="84a63-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="84a63-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84a63-202">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="84a63-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84a63-203">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="84a63-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84a63-204">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84a63-205">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84a63-206">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84a63-207">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84a63-208">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84a63-209">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84a63-210">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84a63-211">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84a63-212">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="84a63-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84a63-213">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84a63-214">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="84a63-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="84a63-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84a63-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="84a63-216">範例</span><span class="sxs-lookup"><span data-stu-id="84a63-216">Examples</span></span>

<span data-ttu-id="84a63-217">[清單登入會話資訊](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3)PowerShell 範例會傳回與目前登入電腦的使用者相關聯之登入會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84a63-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="84a63-218">下列 PowerShell 範例會檢查是否有指定使用者的遠端會話開啟。</span><span class="sxs-lookup"><span data-stu-id="84a63-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="84a63-219">規格需求</span><span class="sxs-lookup"><span data-stu-id="84a63-219">Requirements</span></span>



| <span data-ttu-id="84a63-220">需求</span><span class="sxs-lookup"><span data-stu-id="84a63-220">Requirement</span></span> | <span data-ttu-id="84a63-221">值</span><span class="sxs-lookup"><span data-stu-id="84a63-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84a63-222">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84a63-222">Minimum supported client</span></span><br/> | <span data-ttu-id="84a63-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84a63-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84a63-224">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84a63-224">Minimum supported server</span></span><br/> | <span data-ttu-id="84a63-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84a63-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84a63-226">命名空間</span><span class="sxs-lookup"><span data-stu-id="84a63-226">Namespace</span></span><br/>                | <span data-ttu-id="84a63-227">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84a63-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84a63-228">MOF</span><span class="sxs-lookup"><span data-stu-id="84a63-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84a63-229"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="84a63-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84a63-230">DLL</span><span class="sxs-lookup"><span data-stu-id="84a63-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a63-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a63-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a63-232">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84a63-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a63-233">**Win32 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="84a63-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="84a63-234">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84a63-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

