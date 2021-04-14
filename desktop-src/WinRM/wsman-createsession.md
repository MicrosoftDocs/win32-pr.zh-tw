---
title: 'CreateSession 方法 (WSManDisp .h) '
description: 建立可用於後續網路作業的會話物件。
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- CreateSession 方法 Windows 遠端管理
- CreateSession 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateSession 方法
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508819"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="19f31-106">WSMan. CreateSession 方法</span><span class="sxs-lookup"><span data-stu-id="19f31-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="19f31-107">建立可用於後續網路作業的 [**會話**](session.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="19f31-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f31-108">語法</span><span class="sxs-lookup"><span data-stu-id="19f31-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="19f31-109">參數</span><span class="sxs-lookup"><span data-stu-id="19f31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f31-110">*連接* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19f31-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19f31-111">要連接的通訊協定和服務，包括 IPv4 或 IPv6。</span><span class="sxs-lookup"><span data-stu-id="19f31-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="19f31-112">連接資訊的格式如下： <*傳輸* >< *位址* >< *尾碼*>。</span><span class="sxs-lookup"><span data-stu-id="19f31-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="19f31-113">如需範例，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="19f31-113">For examples, see Remarks.</span></span> <span data-ttu-id="19f31-114">如果未提供任何連接資訊，則會使用本機電腦。</span><span class="sxs-lookup"><span data-stu-id="19f31-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="19f31-115">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19f31-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19f31-116">指定驗證方法的會話旗標，例如用於連接到遠端電腦的驗證方法，例如「 [*協商驗證*](windows-remote-management-glossary.md) 」或「 [*摘要式驗證*](windows-remote-management-glossary.md)」。</span><span class="sxs-lookup"><span data-stu-id="19f31-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="19f31-117">這些旗標也會指定其他會話連接資訊，例如編碼或加密。</span><span class="sxs-lookup"><span data-stu-id="19f31-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="19f31-118">此參數必須包含 **\_ \_ WSManSessionFlags** 中的一或多個旗標以進行遠端連線。</span><span class="sxs-lookup"><span data-stu-id="19f31-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="19f31-119">如需詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="19f31-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="19f31-120">本機電腦上的 WinRM 連接不需要任何旗標設定。</span><span class="sxs-lookup"><span data-stu-id="19f31-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="19f31-121">預設值為 **WSManFlagUseNegotiate**。</span><span class="sxs-lookup"><span data-stu-id="19f31-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="19f31-122">如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md) 和 *connectionOptions* 參數。</span><span class="sxs-lookup"><span data-stu-id="19f31-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19f31-123">*connectionOptions* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19f31-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19f31-124">[**ConnectionOptions**](connectionoptions.md)物件的指標，其中包含使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="19f31-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="19f31-125">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="19f31-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f31-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="19f31-126">Return value</span></span>

<span data-ttu-id="19f31-127">可以用來執行本機或遠端 WinRM 作業的 [**會話**](session.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="19f31-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f31-128">備註</span><span class="sxs-lookup"><span data-stu-id="19f31-128">Remarks</span></span>

<span data-ttu-id="19f31-129">**CreateSession** 方法會藉由收集參數，例如旗標、認證和 *連接* 參數的連接字串，初始化 [**會話**](session.md)物件。</span><span class="sxs-lookup"><span data-stu-id="19f31-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="19f31-130">**CreateSession** 並不會實際連接到本機或遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="19f31-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="19f31-131">如果無法建立連接，則在呼叫 **CreateSession** 之後，第一個 **會話作業**（例如 [**Get**](session-get.md)或 [**列舉**](session-enumerate.md)）會發生失敗。</span><span class="sxs-lookup"><span data-stu-id="19f31-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="19f31-132">此行為不同于與遠端電腦上的 [*命名空間*](windows-remote-management-glossary.md)的 [*WMI*](windows-remote-management-glossary.md)連接。</span><span class="sxs-lookup"><span data-stu-id="19f31-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="19f31-133">如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="19f31-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="19f31-134">下列 VBScript 程式碼範例會用來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="19f31-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="19f31-135">下列範例顯示在建立 HTTPS 會話時，用來指定 *連線參數 (* 中的連接資訊的不同格式、<*位址*> 欄位必須符合伺服器電腦憑證名稱，否則) 發生失敗：</span><span class="sxs-lookup"><span data-stu-id="19f31-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="19f31-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="19f31-136">"https://service"</span></span>

    <span data-ttu-id="19f31-137">使用 HTTPS 連接到預設的 web 服務位置。</span><span class="sxs-lookup"><span data-stu-id="19f31-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="19f31-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="19f31-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="19f31-139">使用 HTTPS 連接到特定的 web 服務位置。</span><span class="sxs-lookup"><span data-stu-id="19f31-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="19f31-140">"HTTPs:// \[ E3D7：0000：0000：0000：51F4：9BC8： C0A8： 6420 \] "</span><span class="sxs-lookup"><span data-stu-id="19f31-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="19f31-141">使用 HTTPS 和 IPv6 搭配預設通訊埠。</span><span class="sxs-lookup"><span data-stu-id="19f31-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="19f31-142">"HTTPs:// \[ E3D7：0000：0000：0000：51F4：9BC8： C0A8： 6420 \] ： 9999/wsman"</span><span class="sxs-lookup"><span data-stu-id="19f31-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="19f31-143">使用 HTTPS 和 IPv6 搭配指定的埠。</span><span class="sxs-lookup"><span data-stu-id="19f31-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="19f31-144">範例</span><span class="sxs-lookup"><span data-stu-id="19f31-144">Examples</span></span>

<span data-ttu-id="19f31-145">下列 VBScript 程式碼範例會在本機電腦上建立會話。</span><span class="sxs-lookup"><span data-stu-id="19f31-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="19f31-146">下列 VBScript 程式碼範例會在以 IP 位址識別的遠端電腦上建立會話。</span><span class="sxs-lookup"><span data-stu-id="19f31-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="19f31-147">腳本會提供帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="19f31-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="19f31-148">**WSManFlagCredUserNamePassword** 和 **WSManFlagUseBasic** 旗標會合並，以指出帳戶是遠端電腦上的本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="19f31-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="19f31-149">如果建立會話失敗，腳本會終止。</span><span class="sxs-lookup"><span data-stu-id="19f31-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="19f31-150">腳本會使用傳回常數的方法，例如 [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)。</span><span class="sxs-lookup"><span data-stu-id="19f31-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="19f31-151">若要執行此腳本，請注意，您必須設定用戶端和伺服器的預設設定，以允許未加密的流量和基本驗證 (**AllowUnencrypted** 設為 **true** ，基本身份設定為 **true**) 。</span><span class="sxs-lookup"><span data-stu-id="19f31-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="19f31-152">如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="19f31-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="19f31-153">在下列 VBScript 程式碼範例中，此帳戶是網域帳戶，而且會使用「協商驗證」。</span><span class="sxs-lookup"><span data-stu-id="19f31-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="19f31-154">使用「協商驗證」時，您必須將使用者名稱指定為 `computername\username` 或 `ipaddress\username` 。</span><span class="sxs-lookup"><span data-stu-id="19f31-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="19f31-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="19f31-155">Requirements</span></span>



| <span data-ttu-id="19f31-156">需求</span><span class="sxs-lookup"><span data-stu-id="19f31-156">Requirement</span></span> | <span data-ttu-id="19f31-157">值</span><span class="sxs-lookup"><span data-stu-id="19f31-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f31-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19f31-158">Minimum supported client</span></span><br/> | <span data-ttu-id="19f31-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19f31-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="19f31-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19f31-160">Minimum supported server</span></span><br/> | <span data-ttu-id="19f31-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f31-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="19f31-162">標頭</span><span class="sxs-lookup"><span data-stu-id="19f31-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f31-163"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="19f31-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="19f31-164">Idl</span><span class="sxs-lookup"><span data-stu-id="19f31-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19f31-165"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="19f31-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="19f31-166">程式庫</span><span class="sxs-lookup"><span data-stu-id="19f31-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="19f31-167"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19f31-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19f31-168">DLL</span><span class="sxs-lookup"><span data-stu-id="19f31-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19f31-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19f31-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19f31-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19f31-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f31-171">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="19f31-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="19f31-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="19f31-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="19f31-173">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="19f31-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="19f31-174">遠端連線的驗證</span><span class="sxs-lookup"><span data-stu-id="19f31-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="19f31-175">Windows 遠端管理的安裝和設定</span><span class="sxs-lookup"><span data-stu-id="19f31-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





