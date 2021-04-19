---
title: IWMPNetwork getProxyPort 方法
description: GetProxyPort 方法會傳回所使用的 proxy 埠。
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- getProxyPort 方法 Windows Media Player
- getProxyPort 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，getProxyPort 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989680"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="42fbe-106">IWMPNetwork：： getProxyPort 方法</span><span class="sxs-lookup"><span data-stu-id="42fbe-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="42fbe-107">**GetProxyPort** 方法會傳回所使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="42fbe-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fbe-108">語法</span><span class="sxs-lookup"><span data-stu-id="42fbe-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="42fbe-109">參數</span><span class="sxs-lookup"><span data-stu-id="42fbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fbe-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42fbe-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fbe-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="42fbe-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="42fbe-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="42fbe-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fbe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="42fbe-113">Return value</span></span>

<span data-ttu-id="42fbe-114">要使用的 proxy 埠的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="42fbe-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="42fbe-115">只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。</span><span class="sxs-lookup"><span data-stu-id="42fbe-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="42fbe-116">備註</span><span class="sxs-lookup"><span data-stu-id="42fbe-116">Remarks</span></span>

<span data-ttu-id="42fbe-117">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="42fbe-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="42fbe-118">範例</span><span class="sxs-lookup"><span data-stu-id="42fbe-118">Examples</span></span>

<span data-ttu-id="42fbe-119">下列程式碼範例會使用 **getProxyPort** 來顯示 MMS 和 HTTP 通訊協定的目前 Windows Media Player proxy 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="42fbe-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="42fbe-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="42fbe-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="42fbe-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="42fbe-121">Requirements</span></span>



| <span data-ttu-id="42fbe-122">需求</span><span class="sxs-lookup"><span data-stu-id="42fbe-122">Requirement</span></span> | <span data-ttu-id="42fbe-123">值</span><span class="sxs-lookup"><span data-stu-id="42fbe-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42fbe-124">版本</span><span class="sxs-lookup"><span data-stu-id="42fbe-124">Version</span></span><br/>   | <span data-ttu-id="42fbe-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="42fbe-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="42fbe-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="42fbe-126">Namespace</span></span><br/> | <span data-ttu-id="42fbe-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="42fbe-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="42fbe-128">組件</span><span class="sxs-lookup"><span data-stu-id="42fbe-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="42fbe-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="42fbe-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42fbe-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42fbe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fbe-131">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="42fbe-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="42fbe-132">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="42fbe-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="42fbe-133">**IWMPNetwork. setProxyPort (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="42fbe-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





