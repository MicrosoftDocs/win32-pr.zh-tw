---
description: 使用腳本存取 Windows Management Instrumentation (WMI) server 時，您可以選擇 NT LAN Manager (NTLM) 或 Kerberos 驗證通訊協定。
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: 使用 VBScript 設定驗證服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975933"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="fb166-103">使用 VBScript 設定驗證服務</span><span class="sxs-lookup"><span data-stu-id="fb166-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="fb166-104">使用腳本存取 Windows Management Instrumentation (WMI) server 時，您可以選擇 NT LAN Manager (NTLM) 或 Kerberos 驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fb166-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="fb166-105">除非使用委派，否則不需要指定 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="fb166-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="fb166-106">如需詳細資訊，請參閱 [連接到第3部電腦委派](connecting-to-a-3rd-computer-delegation.md)。</span><span class="sxs-lookup"><span data-stu-id="fb166-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="fb166-107">因為作業系統版本的不同之處在于其使用的驗證服務，所以建議您不要在連接到遠端系統時指定 [授權單位] 欄位的值。</span><span class="sxs-lookup"><span data-stu-id="fb166-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="fb166-108">相反地，請允許作業系統和分散式版本的元件物件模型 (DCOM) 來選取 NTLM 或 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="fb166-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="fb166-109">如果指定了驗證服務，則語法需要伺服器主體名稱，也就是目的電腦的名稱，而不是網域控制站。</span><span class="sxs-lookup"><span data-stu-id="fb166-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="fb166-110">您只能將授權參數用於遠端 WMI 伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="fb166-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="fb166-111">如果您嘗試將授權層級設定為標記的一部分，或呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 以進行本機連接，連接嘗試就會失敗。</span><span class="sxs-lookup"><span data-stu-id="fb166-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="fb166-112">請執行下列程式，以指定您要在 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)方法的 *strAuthority* 參數中使用的驗證服務，或使用 [標記](constructing-a-moniker-string.md)字串連接。</span><span class="sxs-lookup"><span data-stu-id="fb166-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="fb166-113">**使用適用于 WMI 的腳本 API 來指定 NTLM 或 Kerberos 驗證**</span><span class="sxs-lookup"><span data-stu-id="fb166-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="fb166-114">如果 *strAuthority* 參數的開頭是 "kerberos：" 字串，WMI 會假設字串參考 kerberos 主體名稱，並使用 kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="fb166-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="fb166-115">如果 *strAuthority* 參數的開頭為 "ntlmdomain：" 字串，WMI 會改為使用 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="fb166-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="fb166-116">或者，您可以使用 [部分] 的 [授權單位] 來指定用來連線到 WMI 的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="fb166-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="fb166-117">若要在使用標記時使用 Kerberos 驗證，請包含字串 "核證 = Kerberos："，後面接著主體名稱。</span><span class="sxs-lookup"><span data-stu-id="fb166-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="fb166-118">若要使用 NTLM 驗證，請包含字串 "核證 = ntlmdomain："，後面接著 NTLM 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fb166-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="fb166-119">下列範例會顯示使用主體 "mydomain server" 要求 Kerberos 驗證的標記 \\ 。</span><span class="sxs-lookup"><span data-stu-id="fb166-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="fb166-120">相反地，下列範例會顯示使用「mydomain」網域要求 NTLM 驗證的標記。</span><span class="sxs-lookup"><span data-stu-id="fb166-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



