---
title: IWMPNetwork getProxyBypassForLocal 方法
description: GetProxyBypassForLocal 方法會傳回值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- getProxyBypassForLocal 方法 Windows Media Player
- getProxyBypassForLocal 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，getProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977509"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="e0e6c-106">IWMPNetwork：： getProxyBypassForLocal 方法</span><span class="sxs-lookup"><span data-stu-id="e0e6c-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="e0e6c-107">**GetProxyBypassForLocal** 方法會傳回值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e6c-108">語法</span><span class="sxs-lookup"><span data-stu-id="e0e6c-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="e0e6c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e0e6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e6c-110">*bstrProtocol*</span><span class="sxs-lookup"><span data-stu-id="e0e6c-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e6c-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e6c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0e6c-112">Return value</span></span>

<span data-ttu-id="e0e6c-113">System.string **值，** 指出是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="e0e6c-114">只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e6c-115">備註</span><span class="sxs-lookup"><span data-stu-id="e0e6c-115">Remarks</span></span>

<span data-ttu-id="e0e6c-116">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="e0e6c-117">範例</span><span class="sxs-lookup"><span data-stu-id="e0e6c-117">Examples</span></span>

<span data-ttu-id="e0e6c-118">下列程式碼範例會使用 **getProxyBypassForLocal** 來顯示是否將 Windows Media Player 設定為略過本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="e0e6c-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="e0e6c-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="e0e6c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0e6c-120">Requirements</span></span>



| <span data-ttu-id="e0e6c-121">需求</span><span class="sxs-lookup"><span data-stu-id="e0e6c-121">Requirement</span></span> | <span data-ttu-id="e0e6c-122">值</span><span class="sxs-lookup"><span data-stu-id="e0e6c-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e6c-123">版本</span><span class="sxs-lookup"><span data-stu-id="e0e6c-123">Version</span></span><br/>   | <span data-ttu-id="e0e6c-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e0e6c-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="e0e6c-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="e0e6c-125">Namespace</span></span><br/> | <span data-ttu-id="e0e6c-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="e0e6c-127">組件</span><span class="sxs-lookup"><span data-stu-id="e0e6c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0e6c-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e6c-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e6c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0e6c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e6c-130">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0e6c-131">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0e6c-132">**IWMPNetwork. setProxyBypassForLocal (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





