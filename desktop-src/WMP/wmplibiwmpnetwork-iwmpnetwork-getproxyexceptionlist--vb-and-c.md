---
title: IWMPNetwork getProxyExceptionList 方法
description: GetProxyExceptionList 方法會傳回 proxy 例外清單。
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- getProxyExceptionList 方法 Windows Media Player
- getProxyExceptionList 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，getProxyExceptionList 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988657"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="40e03-106">IWMPNetwork：： getProxyExceptionList 方法</span><span class="sxs-lookup"><span data-stu-id="40e03-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="40e03-107">**GetProxyExceptionList** 方法會傳回 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="40e03-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e03-108">語法</span><span class="sxs-lookup"><span data-stu-id="40e03-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="40e03-109">參數</span><span class="sxs-lookup"><span data-stu-id="40e03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40e03-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40e03-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40e03-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="40e03-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="40e03-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="40e03-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40e03-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="40e03-113">Return value</span></span>

<span data-ttu-id="40e03-114">**System.string** ，這是略過 proxy 伺服器的主機清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="40e03-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="40e03-115">只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。</span><span class="sxs-lookup"><span data-stu-id="40e03-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="40e03-116">備註</span><span class="sxs-lookup"><span data-stu-id="40e03-116">Remarks</span></span>

<span data-ttu-id="40e03-117">當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="40e03-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="40e03-118">\*字元可以用來做為清單專案的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="40e03-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="40e03-119">例如， \* .com 會比對 com 網域中的所有主機，而67則 \* 會比對67類別中的所有主機與子網。</span><span class="sxs-lookup"><span data-stu-id="40e03-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="40e03-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="40e03-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="40e03-121">範例</span><span class="sxs-lookup"><span data-stu-id="40e03-121">Examples</span></span>

<span data-ttu-id="40e03-122">下列程式碼範例會使用 **getProxyExceptionList** 來顯示是否將 Windows Media Player 設定為略過本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="40e03-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="40e03-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="40e03-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="40e03-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="40e03-124">Requirements</span></span>



| <span data-ttu-id="40e03-125">需求</span><span class="sxs-lookup"><span data-stu-id="40e03-125">Requirement</span></span> | <span data-ttu-id="40e03-126">值</span><span class="sxs-lookup"><span data-stu-id="40e03-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40e03-127">版本</span><span class="sxs-lookup"><span data-stu-id="40e03-127">Version</span></span><br/>   | <span data-ttu-id="40e03-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="40e03-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="40e03-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="40e03-129">Namespace</span></span><br/> | <span data-ttu-id="40e03-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="40e03-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="40e03-131">組件</span><span class="sxs-lookup"><span data-stu-id="40e03-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="40e03-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="40e03-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40e03-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40e03-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e03-134">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="40e03-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="40e03-135">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="40e03-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="40e03-136">**IWMPNetwork. setProxyExceptionList (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="40e03-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





