---
title: IWMPNetwork getProxyName 方法
description: GetProxyName 方法會傳回所使用 proxy 伺服器的名稱。
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- getProxyName 方法 Windows Media Player
- getProxyName 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，getProxyName 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997668"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="98f87-106">IWMPNetwork：： getProxyName 方法</span><span class="sxs-lookup"><span data-stu-id="98f87-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="98f87-107">**GetProxyName** 方法會傳回所使用 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f87-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f87-108">語法</span><span class="sxs-lookup"><span data-stu-id="98f87-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="98f87-109">參數</span><span class="sxs-lookup"><span data-stu-id="98f87-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f87-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98f87-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f87-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="98f87-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="98f87-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="98f87-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f87-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="98f87-113">Return value</span></span>

<span data-ttu-id="98f87-114">**System.string** ，這是所使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="98f87-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="98f87-115">只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。</span><span class="sxs-lookup"><span data-stu-id="98f87-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="98f87-116">備註</span><span class="sxs-lookup"><span data-stu-id="98f87-116">Remarks</span></span>

<span data-ttu-id="98f87-117">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="98f87-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="98f87-118">範例</span><span class="sxs-lookup"><span data-stu-id="98f87-118">Examples</span></span>

<span data-ttu-id="98f87-119">下列程式碼範例會使用 **getProxyName** 來顯示 HTTP 和 MMS 通訊協定的 Windows Media Player proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="98f87-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="98f87-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="98f87-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="98f87-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="98f87-121">Requirements</span></span>



| <span data-ttu-id="98f87-122">需求</span><span class="sxs-lookup"><span data-stu-id="98f87-122">Requirement</span></span> | <span data-ttu-id="98f87-123">值</span><span class="sxs-lookup"><span data-stu-id="98f87-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f87-124">版本</span><span class="sxs-lookup"><span data-stu-id="98f87-124">Version</span></span><br/>   | <span data-ttu-id="98f87-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="98f87-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="98f87-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="98f87-126">Namespace</span></span><br/> | <span data-ttu-id="98f87-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="98f87-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="98f87-128">組件</span><span class="sxs-lookup"><span data-stu-id="98f87-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98f87-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="98f87-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f87-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98f87-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f87-131">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98f87-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98f87-132">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98f87-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98f87-133">**IWMPNetwork. setProxyName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="98f87-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





