---
title: 偵測遠端電腦是否支援 WS-Management 的通訊協定
description: 您可以使用此會話。識別或 Iwsmansession.invoke。識別方法以判斷遠端電腦是否有支援 WS-Management 通訊協定的服務。
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967425"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="9493c-103">偵測遠端電腦是否支援 WS-Management 的通訊協定</span><span class="sxs-lookup"><span data-stu-id="9493c-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="9493c-104">您可以使用此 [**會話。**](session-identify.md) 識別或 [**iwsmansession.invoke。識別**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) 方法以判斷遠端電腦是否有支援 WS-Management 通訊協定的服務。</span><span class="sxs-lookup"><span data-stu-id="9493c-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="9493c-105">如果在遠端電腦上設定了 WS-Management 的通訊協定服務，並且正在接聽要求，則服務可以透過標頭中的下列 XML 來偵測識別要求。</span><span class="sxs-lookup"><span data-stu-id="9493c-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="9493c-106">接收要求的 WS-Management 通訊協定服務會在訊息本文中傳回下列清單中所包含的資訊：</span><span class="sxs-lookup"><span data-stu-id="9493c-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="9493c-107">WS-Management 的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="9493c-107">The WS-Management protocol version.</span></span> <span data-ttu-id="9493c-108">例如，"https://schemas.dmtf.org/wbem/wsman/1/wsman"。</span><span class="sxs-lookup"><span data-stu-id="9493c-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="9493c-109">產品廠商，例如「Microsoft Corporation」。</span><span class="sxs-lookup"><span data-stu-id="9493c-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="9493c-110">產品版本。</span><span class="sxs-lookup"><span data-stu-id="9493c-110">The product version.</span></span> <span data-ttu-id="9493c-111">如果在 *旗標* 參數中使用 **WSManFlagUseNoAuthentication** 傳送要求，則不會傳回任何產品版本資訊。</span><span class="sxs-lookup"><span data-stu-id="9493c-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="9493c-112">如果要求是以作用中的預設驗證或指定的另一個驗證模式來傳送，則可以傳回產品版本資訊。</span><span class="sxs-lookup"><span data-stu-id="9493c-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="9493c-113">偵測遠端電腦是否有設定和接聽 WS-Management 通訊協定服務的要求，可以在腳本開頭與其他作業中執行。</span><span class="sxs-lookup"><span data-stu-id="9493c-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="9493c-114">這會確認目的電腦是否可以回應進一步 WS-Management 的通訊協定要求。</span><span class="sxs-lookup"><span data-stu-id="9493c-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="9493c-115">您也可以在個別的腳本中進行驗證。</span><span class="sxs-lookup"><span data-stu-id="9493c-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="9493c-116">**偵測 WS-Management 的通訊協定服務**</span><span class="sxs-lookup"><span data-stu-id="9493c-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="9493c-117">建立 [**WSMan**](wsman.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9493c-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="9493c-118">判斷是否應將要求傳送至已驗證或未驗證，並且在 [**CreateSession**](wsman-createsession.md)的呼叫中適當地設定 *flags* 參數。</span><span class="sxs-lookup"><span data-stu-id="9493c-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="9493c-119">呼叫 [**會話。識別**](session-identify.md)。</span><span class="sxs-lookup"><span data-stu-id="9493c-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="9493c-120">範例</span><span class="sxs-lookup"><span data-stu-id="9493c-120">Examples</span></span>

<span data-ttu-id="9493c-121">下列 VBScript 程式碼範例會將未經驗證的識別要求傳送至相同網域中名為 "Remote1" 的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="9493c-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="9493c-122">下列回應會顯示遠端電腦所傳回的 XML。</span><span class="sxs-lookup"><span data-stu-id="9493c-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="9493c-123">WS-Management 通訊協定版本 ( " https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd " ) 和作業系統廠商 ( "Microsoft Corporation" ) 是在傳回的 XML 中指定。</span><span class="sxs-lookup"><span data-stu-id="9493c-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="9493c-124">因為訊息會以未驗證的方式傳送，Windows 遠端管理服務不會傳回產品版本。</span><span class="sxs-lookup"><span data-stu-id="9493c-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="9493c-125">下列 VBScript 程式碼範例會將已驗證的識別要求傳送至遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="9493c-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="9493c-126">由於要求是以驗證傳送，因此會傳回版本資訊。</span><span class="sxs-lookup"><span data-stu-id="9493c-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="9493c-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9493c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9493c-128">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="9493c-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9493c-129">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="9493c-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9493c-130">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="9493c-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




