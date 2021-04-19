---
description: 連接到在 strServer 參數中指定之電腦上的命名空間。
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: 'Wbemscripting.swbemlocator. ConnectServer 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987790"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="73aa5-103">Wbemscripting.swbemlocator. ConnectServer 方法</span><span class="sxs-lookup"><span data-stu-id="73aa5-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="73aa5-104">[**Wbemscripting.swbemlocator**](swbemlocator.md)物件的 **ConnectServer** 方法會連接到 *strServer* 參數中指定之電腦上的命名空間。</span><span class="sxs-lookup"><span data-stu-id="73aa5-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="73aa5-105">目的電腦可以是本機或遠端，但必須安裝 WMI。</span><span class="sxs-lookup"><span data-stu-id="73aa5-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="73aa5-106">如需範例以及與連接的 [標記類型] 的比較，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="73aa5-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="73aa5-107">從 Windows Vista 開始， **wbemscripting.swbemlocator** 可以使用 *strServer* 參數中的 ipv6 位址，連線到執行 ipv6 的電腦。</span><span class="sxs-lookup"><span data-stu-id="73aa5-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="73aa5-108">如需詳細資訊，請參閱 [WMI 中的 IPv6 和 IPv4 支援](ipv6-and-ipv4-support-in-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="73aa5-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="73aa5-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="73aa5-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="73aa5-110">語法</span><span class="sxs-lookup"><span data-stu-id="73aa5-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="73aa5-111">參數</span><span class="sxs-lookup"><span data-stu-id="73aa5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73aa5-112">*strServer* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-113">您要連接的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="73aa5-114">如果遠端電腦與您用來登入的使用者帳戶位於不同的網域，請使用完整的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="73aa5-115">如果您未提供此參數，則呼叫會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="73aa5-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="73aa5-116">範例： `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="73aa5-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="73aa5-117">您也可以在此參數中使用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="73aa5-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="73aa5-118">如果 IP 位址是 IPv6 格式，目的電腦必須執行 IPv6。</span><span class="sxs-lookup"><span data-stu-id="73aa5-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="73aa5-119">IPv4 中的位址看起來像 `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="73aa5-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="73aa5-120">IPv6 格式的 IP 位址看起來像 `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="73aa5-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="73aa5-121">如需有關 DNS 和 IPv4 的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="73aa5-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-122">*strNamespace* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-123">字串，指定您登入的命名空間。</span><span class="sxs-lookup"><span data-stu-id="73aa5-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="73aa5-124">例如，若要登入根 \\ 預設命名空間，請使用根 \\ 預設值。</span><span class="sxs-lookup"><span data-stu-id="73aa5-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="73aa5-125">如果您未指定此參數，它會預設為設定為腳本之預設命名空間的命名空間。</span><span class="sxs-lookup"><span data-stu-id="73aa5-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="73aa5-126">如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="73aa5-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="73aa5-127">範例：「根 \\ CIMV2」</span><span class="sxs-lookup"><span data-stu-id="73aa5-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-128">*strUser* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-129">要用來連接的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-129">User name to use to connect.</span></span> <span data-ttu-id="73aa5-130">字串的格式可以是使用者名稱或網域使用者名稱 \\ 。</span><span class="sxs-lookup"><span data-stu-id="73aa5-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="73aa5-131">將此參數保留空白，以使用目前的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="73aa5-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="73aa5-132">*StrUser* 參數只能搭配遠端 WMI 伺服器的連接使用。</span><span class="sxs-lookup"><span data-stu-id="73aa5-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="73aa5-133">如果您嘗試指定本機 WMI 連接的 *strUser* ，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="73aa5-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="73aa5-134">如果使用 Kerberos 驗證，則無法在網路上攔截 *strUser* 和 *strPassword* 中指定的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="73aa5-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="73aa5-135">您可以使用 UPN 格式來指定 *strUser*。</span><span class="sxs-lookup"><span data-stu-id="73aa5-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="73aa5-136">範例： "DomainName \\ UserName"</span><span class="sxs-lookup"><span data-stu-id="73aa5-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="73aa5-137">如果在 *strAuthority* 中指定網域，則不得在此指定網域。</span><span class="sxs-lookup"><span data-stu-id="73aa5-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="73aa5-138">在這兩個參數中指定定義域會導致不正確參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="73aa5-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="73aa5-139">*strPassword* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-140">字串，指定嘗試連接時要使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="73aa5-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="73aa5-141">將參數保留空白，以使用目前的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="73aa5-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="73aa5-142">*StrPassword* 參數只能搭配遠端 WMI 伺服器的連接使用。</span><span class="sxs-lookup"><span data-stu-id="73aa5-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="73aa5-143">如果您嘗試指定本機 WMI 連接的 *strPassword* ，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="73aa5-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="73aa5-144">如果使用 Kerberos 驗證，則無法在網路上攔截 *strUser* 和 *strPassword* 中指定的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="73aa5-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-145">*strLocale* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-146">指定當地語系化程式碼的字串。</span><span class="sxs-lookup"><span data-stu-id="73aa5-146">String that specifies the localization code.</span></span> <span data-ttu-id="73aa5-147">如果您想要使用目前的地區設定，請將其保留空白。</span><span class="sxs-lookup"><span data-stu-id="73aa5-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="73aa5-148">如果不是空白，則此參數必須是字串，指出必須在其中取出資訊的所需地區設定。</span><span class="sxs-lookup"><span data-stu-id="73aa5-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="73aa5-149">若為 Microsoft 地區設定識別碼，則字串的格式為 "MS \_ xxxx"，其中 xxxx 是十六進位格式的字串，表示 LCID。</span><span class="sxs-lookup"><span data-stu-id="73aa5-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="73aa5-150">例如，美式英文會顯示為「MS \_ 409」。</span><span class="sxs-lookup"><span data-stu-id="73aa5-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-151">*strAuthority* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="73aa5-152">""</span><span class="sxs-lookup"><span data-stu-id="73aa5-152">""</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-153">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="73aa5-153">This parameter is optional.</span></span> <span data-ttu-id="73aa5-154">但是，如果指定了，則只能使用 Kerberos 或 NTLMDomain。</span><span class="sxs-lookup"><span data-stu-id="73aa5-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-155">Kerberos：</span><span class="sxs-lookup"><span data-stu-id="73aa5-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-156">如果 *strAuthority* 參數的開頭是 "Kerberos：" 字串，則會使用 kerberos 驗證，且此參數應包含 kerberos 主體名稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="73aa5-157">Kerberos 主體名稱會指定為 Kerberos：*domain*，例如 `Kerberos:fabrikam` `fabrikam` 您嘗試連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="73aa5-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="73aa5-158">範例： "Kerberos： DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="73aa5-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-159">NTLMDomain</span><span class="sxs-lookup"><span data-stu-id="73aa5-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-160">若要使用 NT Lan Manager (NTLM) 驗證，您必須將它指定為 NTLMDomain：*domain*，例如 `NTLMDomain:fabrikam` where `fabrikam` 是網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="73aa5-161">範例： "NTLMDomain： DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="73aa5-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="73aa5-162">如果您將此參數保留空白，作業系統會與 COM 協商，以決定是否要使用 NTLM 或 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="73aa5-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="73aa5-163">這個參數只能與遠端 WMI 伺服器的連接搭配使用。</span><span class="sxs-lookup"><span data-stu-id="73aa5-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="73aa5-164">如果您嘗試設定本機 WMI 連接的授權單位，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="73aa5-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="73aa5-165">如果網域是在 *strUser* 中指定，這是慣用的位置，則不得在此指定。</span><span class="sxs-lookup"><span data-stu-id="73aa5-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="73aa5-166">在這兩個參數中指定定義域會導致不正確參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="73aa5-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="73aa5-167">*iSecurityFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-168">用來將旗標值傳遞至 **ConnectServer**。</span><span class="sxs-lookup"><span data-stu-id="73aa5-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="73aa5-169">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="73aa5-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-170">這個參數的值為0，只會在建立伺服器的連接之後，才傳回 **ConnectServer** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="73aa5-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="73aa5-171">如果無法建立連線，這可能會導致您的程式無限期停止回應。</span><span class="sxs-lookup"><span data-stu-id="73aa5-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="73aa5-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="73aa5-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="73aa5-173">**ConnectServer** 呼叫保證會在2分鐘以內傳回。</span><span class="sxs-lookup"><span data-stu-id="73aa5-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="73aa5-174">如果無法建立連線，請使用此旗標來防止您的程式停止無限期地回應。</span><span class="sxs-lookup"><span data-stu-id="73aa5-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="73aa5-175">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73aa5-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-176">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="73aa5-176">Typically, this is undefined.</span></span> <span data-ttu-id="73aa5-177">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="73aa5-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="73aa5-178">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="73aa5-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73aa5-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="73aa5-179">Return value</span></span>

<span data-ttu-id="73aa5-180">如果成功，WMI 會傳回 [**SWbemServices**](swbemservices.md)物件，該物件系結至 *strServer* 中指定之電腦上的 *strNamespace* 中指定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="73aa5-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73aa5-181">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="73aa5-181">Error codes</span></span>

<span data-ttu-id="73aa5-182">**ConnectServer** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73aa5-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="73aa5-183">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="73aa5-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-184">目前或指定的使用者名稱和密碼無效或已獲授權，無法進行連接。</span><span class="sxs-lookup"><span data-stu-id="73aa5-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-185">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="73aa5-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-186">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="73aa5-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100E) </span><span class="sxs-lookup"><span data-stu-id="73aa5-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-188">指定的命名空間不存在於伺服器上。</span><span class="sxs-lookup"><span data-stu-id="73aa5-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-189">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="73aa5-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-190">指定的參數無效，或無法剖析命名空間。</span><span class="sxs-lookup"><span data-stu-id="73aa5-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-191">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="73aa5-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-192">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="73aa5-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="73aa5-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="73aa5-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="73aa5-194">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="73aa5-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73aa5-195">備註</span><span class="sxs-lookup"><span data-stu-id="73aa5-195">Remarks</span></span>

<span data-ttu-id="73aa5-196">當您在遠端電腦上使用不同的使用者名稱和密碼認證連接到帳戶時，通常會使用 **ConnectServer** 方法，因為您無法在 [標記](constructing-a-moniker-string.md) 字串中指定不同的密碼。</span><span class="sxs-lookup"><span data-stu-id="73aa5-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="73aa5-197">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="73aa5-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="73aa5-198">使用 IPv4 位址連線到遠端伺服器可能會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="73aa5-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="73aa5-199">可能的原因是您的環境中有過時的 DNS 專案。</span><span class="sxs-lookup"><span data-stu-id="73aa5-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="73aa5-200">在這些情況下，將會使用機器的過時 PTR 專案，並產生無法預測的結果。</span><span class="sxs-lookup"><span data-stu-id="73aa5-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="73aa5-201">若要避免此行為，您可以將句點附加 ( "."在呼叫 ConnectServer 之前 ) 至 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="73aa5-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="73aa5-202">這會導致反向 DNS 查閱失敗，但可能會允許在正確的電腦上成功 **ConnectServer** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="73aa5-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="73aa5-203">範例</span><span class="sxs-lookup"><span data-stu-id="73aa5-203">Examples</span></span>

<span data-ttu-id="73aa5-204">下列 VBScript 程式碼範例說明如何連接到遠端電腦，以取得 [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) 資料。</span><span class="sxs-lookup"><span data-stu-id="73aa5-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="73aa5-205">在 *strAuthority* 中使用 *strDomain* 中指定的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="73aa5-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="73aa5-206">下列 PowerShell 程式碼片段會存取遠端伺服器，並列出可用的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="73aa5-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="73aa5-207">規格需求</span><span class="sxs-lookup"><span data-stu-id="73aa5-207">Requirements</span></span>



| <span data-ttu-id="73aa5-208">需求</span><span class="sxs-lookup"><span data-stu-id="73aa5-208">Requirement</span></span> | <span data-ttu-id="73aa5-209">值</span><span class="sxs-lookup"><span data-stu-id="73aa5-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73aa5-210">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73aa5-210">Minimum supported client</span></span><br/> | <span data-ttu-id="73aa5-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73aa5-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73aa5-212">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73aa5-212">Minimum supported server</span></span><br/> | <span data-ttu-id="73aa5-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73aa5-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73aa5-214">標頭</span><span class="sxs-lookup"><span data-stu-id="73aa5-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="73aa5-215"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="73aa5-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="73aa5-216">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="73aa5-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="73aa5-217"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73aa5-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73aa5-218">DLL</span><span class="sxs-lookup"><span data-stu-id="73aa5-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73aa5-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73aa5-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="73aa5-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="73aa5-220">CLSID</span></span><br/>                    | <span data-ttu-id="73aa5-221">CLSID \_ wbemscripting.swbemlocator</span><span class="sxs-lookup"><span data-stu-id="73aa5-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="73aa5-222">IID</span><span class="sxs-lookup"><span data-stu-id="73aa5-222">IID</span></span><br/>                      | <span data-ttu-id="73aa5-223">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="73aa5-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="73aa5-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73aa5-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73aa5-225">**Wbemscripting.swbemlocator**</span><span class="sxs-lookup"><span data-stu-id="73aa5-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="73aa5-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="73aa5-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="73aa5-227">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="73aa5-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="73aa5-228">建立 WMI 腳本</span><span class="sxs-lookup"><span data-stu-id="73aa5-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

