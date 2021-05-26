---
title: ADSI 中的事件追蹤
description: Windows Server 2008 和 Windows Vista 引進 Active Directory 服務介面 (ADSI) 的事件追蹤。
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- 事件追蹤 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423708"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="b2f3c-104">ADSI 中的事件追蹤</span><span class="sxs-lookup"><span data-stu-id="b2f3c-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="b2f3c-105">Windows Server 2008 和 Windows Vista 引進[Active Directory 服務介面](active-directory-service-interfaces-adsi.md) (ADSI) 的[事件追蹤](/windows/desktop/ETW/event-tracing-portal)。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="b2f3c-106">ADSI LDAP 提供者的某些區域具有複雜的基礎執行，或牽涉到的一連串步驟，讓您難以診斷問題。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="b2f3c-107">為了協助應用程式開發人員進行疑難排解，事件追蹤已新增至下欄區域：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="b2f3c-108">架構剖析和下載</span><span class="sxs-lookup"><span data-stu-id="b2f3c-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="b2f3c-109">ADSI 中的 IADs 介面需要在用戶端上快取 LDAP 架構，如此一來，就可以正確地封送處理屬性 (，如 [ADSI 架構模型](adsi-schema-model.md)) 中所述。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="b2f3c-110">為了達成此目的，ADSI 會將每個處理常式的架構載入 (，並將每個 LDAP 伺服器/網域) 至記憶體中，從儲存在本機磁片上的架構 ( .sch) 檔案，或從 LDAP 伺服器下載。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="b2f3c-111">相同用戶端電腦上的不同進程會使用磁片上的快取架構（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="b2f3c-112">如果無法從磁片或伺服器取得架構，ADSI 會使用硬式編碼的預設架構。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="b2f3c-113">發生這種情況時，無法封送處理不屬於這個預設架構的屬性，而且 ADSI 在抓取這些屬性時會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="b2f3c-114">有許多因素可能會導致這種情況發生，包括剖析架構時發生問題，以及沒有足夠的許可權可下載架構。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="b2f3c-115">通常很難判斷為何會使用特定的預設架構。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="b2f3c-116">在此區域使用事件追蹤將有助於更快速地診斷問題並加以修正。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="b2f3c-117">變更和設定密碼</span><span class="sxs-lookup"><span data-stu-id="b2f3c-117">Changing and Setting the Password</span></span>

<span data-ttu-id="b2f3c-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) 和 [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) 採用多個機制，根據可用的設定 (來執行要求的作業，如 [設定和變更使用者密碼與 LDAP 提供者](setting-user-passwords-for-ldap-providers.md)) 中所述。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="b2f3c-119">當 **ChangePassword** 和 **SetPassword** 失敗時，很難判斷確切的原因，而事件追蹤將有助於疑難排解這些方法的問題。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="b2f3c-120">ADSI 系結快取</span><span class="sxs-lookup"><span data-stu-id="b2f3c-120">ADSI Bind Cache</span></span>

<span data-ttu-id="b2f3c-121">ADSI 會在內部嘗試重複使用 LDAP 連線， (查看 [連接](connection-caching.md) 快取) 。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="b2f3c-122">進行疑難排解時，追蹤是否已開啟新連接來與伺服器通訊，或是否使用現有的連接，是很有用的。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="b2f3c-123">這也有助於追蹤連線快取的生命週期 (有時也稱為系結快取) 和它的建立或關閉，以及是否發生連接的參考。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="b2f3c-124">在 [無伺服器](/windows/desktop/AD/serverless-binding-and-rootdse)系結的情況下，ADSI 會呼叫 DC 定位器來選取使用者內容網域的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="b2f3c-125">然後，ADSI 會維持網域伺服器對應的快取，以便進行後續連接。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="b2f3c-126">事件追蹤有助於追蹤選取的 DC，因此有助於疑難排解連接相關的問題。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="b2f3c-127">啟用追蹤和啟動追蹤會話</span><span class="sxs-lookup"><span data-stu-id="b2f3c-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="b2f3c-128">若要開啟 ADSI 追蹤，請建立下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="b2f3c-129">**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **追蹤** \\ **_ProcessName_**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="b2f3c-130">*ProcessName* 是您要追蹤之進程的完整名稱，包括其延伸 (例如「Svchost.exe」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="b2f3c-131">此外，您可以在此機碼中放入名為的 **DWORD** 類型的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="b2f3c-132">強烈建議您設定此值，因此只會追蹤特定的進程。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="b2f3c-133">否則，將會追蹤 *ProcessName* 所指定之應用程式的所有實例。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="b2f3c-134">然後執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-134">Then execute the following command:</span></span>

<span data-ttu-id="b2f3c-135">**tracelog.exe-開始\*\*\*會話* 名稱 **- \# guid**_提供者 \_ guid_ **-f** *檔案名* **-旗** 標 *追蹤旗標\*\*\*層級** *traceLevel*</span><span class="sxs-lookup"><span data-stu-id="b2f3c-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="b2f3c-136">*sessionname* 只是用來標示追蹤會話的任意識別碼 (您稍後在停止追蹤會話) 時，必須參考此會話名稱。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="b2f3c-137">ADSI 追蹤提供者的 GUID 是「7288c9f8-d63c-4932-a345-89d6b060174d」。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="b2f3c-138">*filename* 會指定要寫入事件的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="b2f3c-139">*追蹤旗標* 必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="b2f3c-140">旗標</span><span class="sxs-lookup"><span data-stu-id="b2f3c-140">Flag</span></span>                        |         <span data-ttu-id="b2f3c-141">值</span><span class="sxs-lookup"><span data-stu-id="b2f3c-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="b2f3c-142">**DEBUG \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="b2f3c-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b2f3c-143">0x00000001</span></span><br/> |
| <span data-ttu-id="b2f3c-144">**DEBUG \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="b2f3c-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b2f3c-145">0x00000002</span></span><br/> |
| <span data-ttu-id="b2f3c-146">**DEBUG \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="b2f3c-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b2f3c-147">0x00000004</span></span><br/> |
| <span data-ttu-id="b2f3c-148">**DEBUG \_ BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="b2f3c-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b2f3c-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="b2f3c-150">這些旗標會根據下表來決定要追蹤的 [ADSI](active-directory-service-interfaces-adsi.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2f3c-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="b2f3c-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2f3c-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="b2f3c-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="b2f3c-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="b2f3c-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="b2f3c-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="b2f3c-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="b2f3c-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="b2f3c-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="b2f3c-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="b2f3c-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="b2f3c-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="b2f3c-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="b2f3c-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="b2f3c-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="b2f3c-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="b2f3c-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="b2f3c-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="b2f3c-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="b2f3c-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="b2f3c-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="b2f3c-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="b2f3c-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="b2f3c-163">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="b2f3c-163">DirectoryString</span></span></li>
<li><span data-ttu-id="b2f3c-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="b2f3c-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="b2f3c-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="b2f3c-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2f3c-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="b2f3c-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2f3c-167">CADsUser：： ChangePassword</span><span class="sxs-lookup"><span data-stu-id="b2f3c-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2f3c-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="b2f3c-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2f3c-169">CADsUser：： SetPassword</span><span class="sxs-lookup"><span data-stu-id="b2f3c-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2f3c-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="b2f3c-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2f3c-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="b2f3c-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="b2f3c-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="b2f3c-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="b2f3c-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="b2f3c-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="b2f3c-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="b2f3c-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="b2f3c-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="b2f3c-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="b2f3c-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="b2f3c-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="b2f3c-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="b2f3c-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="b2f3c-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="b2f3c-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="b2f3c-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="b2f3c-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="b2f3c-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="b2f3c-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="b2f3c-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="b2f3c-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="b2f3c-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="b2f3c-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="b2f3c-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="b2f3c-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="b2f3c-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="b2f3c-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="b2f3c-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="b2f3c-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="b2f3c-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="b2f3c-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="b2f3c-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="b2f3c-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b2f3c-188">您可以藉由在 *追蹤旗標* 引數中結合適當的位來合併旗標。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="b2f3c-189">例如，若要指定 **debug \_ SCHEMA** 和 **debug \_ BINDCACHE** 旗標，則會0x00000009 適當的 *追蹤旗標* 值。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="b2f3c-190">最後， *traceLevel* 旗標應為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="b2f3c-191">旗標</span><span class="sxs-lookup"><span data-stu-id="b2f3c-191">Flag</span></span>                                    |       <span data-ttu-id="b2f3c-192">值</span><span class="sxs-lookup"><span data-stu-id="b2f3c-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="b2f3c-193">**追蹤 \_ 層級 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="b2f3c-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b2f3c-194">0x00000002</span></span><br/> |
| <span data-ttu-id="b2f3c-195">**追蹤 \_ 層級 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="b2f3c-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b2f3c-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="b2f3c-197">**追蹤 \_層級 \_ 資訊** 會導致追蹤處理常式記錄所有事件，而 **追蹤 \_ 層級的 \_ 錯誤** 會導致追蹤進程只記錄錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="b2f3c-198">若要終止追蹤，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="b2f3c-199">**tracelog.exe-停止** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="b2f3c-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="b2f3c-200">在上述範例中， *sessionname* 與啟動追蹤區段的命令所提供的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f3c-201">備註</span><span class="sxs-lookup"><span data-stu-id="b2f3c-201">Remarks</span></span>

<span data-ttu-id="b2f3c-202">藉由指定特定的 PID，而不是追蹤電腦上的所有處理常式，更有效地追蹤特定的進程。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="b2f3c-203">如果您需要追蹤相同電腦上的多個應用程式，可能會對效能造成影響。程式碼的效能導向區段中有大量的偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="b2f3c-204">此外，在追蹤多個進程時，系統管理員必須小心地設定記錄檔的許可權;否則，任何使用者都可以讀取追蹤記錄，而其他使用者可以追蹤包含安全資訊的處理常式。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="b2f3c-205">例如，假設系統管理員設定應用程式 "Test.exe" 的追蹤，而且未在登錄中指定 PID 來追蹤處理常式的多個實例。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="b2f3c-206">現在另一位使用者想要追蹤應用程式「Secure.exe」。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="b2f3c-207">如果追蹤記錄檔未受到適當限制，則該使用者必須做的就是將 "Secure.exe" 重新命名為 "Test.exe"，並且將會進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="b2f3c-208">一般而言，最好只在進行疑難排解時追蹤特定的進程，並在進行疑難排解時立即移除追蹤登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="b2f3c-209">由於啟用事件追蹤將會產生額外的記錄檔，因此系統管理員應謹慎地監視記錄檔大小;本機電腦上的磁碟空間不足可能會造成拒絕服務。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="b2f3c-210">範例案例</span><span class="sxs-lookup"><span data-stu-id="b2f3c-210">Example Scenarios</span></span>

<span data-ttu-id="b2f3c-211">案例1：系統管理員在應用程式中看到未預期的錯誤，此應用程式會設定使用者帳戶的密碼，因此它們會採取下列步驟來使用事件追蹤來修正問題。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="b2f3c-212">撰寫可重現問題的腳本，並建立登錄機碼</span><span class="sxs-lookup"><span data-stu-id="b2f3c-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="b2f3c-213">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="b2f3c-214">使用下列命令，啟動追蹤會話、將 *追蹤旗標* 設定為 0X2 (**DEBUG \_ CHANGEPASSWD**) 和 *traceLevel* to 0x4 (**追蹤 \_ 層級 \_ 資訊**) ：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="b2f3c-215">**tracelog.exe-start scripttrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\adsi-旗標 0x2-層級0x4**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="b2f3c-216">使用測試腳本執行 cscript.exe，以重現問題，然後終止追蹤會話：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="b2f3c-217">**tracelog.exe-停止 scripttrace**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="b2f3c-218">刪除登錄機碼</span><span class="sxs-lookup"><span data-stu-id="b2f3c-218">Delete the registry key</span></span>

    <span data-ttu-id="b2f3c-219">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="b2f3c-220">執行 ETW 工具 Tracerpt.exe，以剖析記錄檔中的追蹤資訊：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="b2f3c-221">**tracelog.exe-start scripttrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\adsi-旗標 0x2-層級0x4**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="b2f3c-222">案例2：系統管理員想要在名為 w3wp.exe 且已在執行中的 [ASP](https://msdn.microsoft.com/asp.net/default.aspx) 應用程式中，追蹤架構剖析和下載作業。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="b2f3c-223">若要這樣做，系統管理員會採取下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="b2f3c-224">建立登錄機碼</span><span class="sxs-lookup"><span data-stu-id="b2f3c-224">Create the registry key</span></span>

    <span data-ttu-id="b2f3c-225">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **adsi** \\ **追蹤** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="b2f3c-226">在該索引鍵中，建立名為 PID 的類型值，並將它設定為目前在本機電腦上執行之 w3wp.exe 實例的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="b2f3c-227">然後，他們會建立追蹤會話、將 *追蹤旗標* 設定為 0X1 (**DEBUG \_ SCHEMA**) 和 *traceLevel* to 0x4 (**追蹤 \_ 層級 \_ 資訊**) ：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="b2f3c-228">**tracelog.exe-start w3wptrace-guid \# 7288c9f8-d63c-4932-a345-89d6b060174d-f。 \\w3wp.exe .etl-旗標 0x1-層級0x4**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="b2f3c-229">重現需要疑難排解的操作。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="b2f3c-230">終止追蹤會話：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="b2f3c-231">**tracelog.exe-停止 w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="b2f3c-232">刪除登錄機碼 **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **追蹤** \\ **w3wp.exe**。</span><span class="sxs-lookup"><span data-stu-id="b2f3c-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="b2f3c-233">執行 ETW 工具 tracerpt.exe，以剖析記錄檔中的追蹤資訊：</span><span class="sxs-lookup"><span data-stu-id="b2f3c-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="b2f3c-234">**tracerpt.exe。 \\w3wp.exe .etl-o-報告**</span><span class="sxs-lookup"><span data-stu-id="b2f3c-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

