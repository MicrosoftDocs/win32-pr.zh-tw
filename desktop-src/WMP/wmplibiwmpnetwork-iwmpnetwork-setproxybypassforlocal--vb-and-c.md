---
title: IWMPNetwork setProxyBypassForLocal 方法
description: SetProxyBypassForLocal 方法會指定如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- setProxyBypassForLocal 方法 Windows Media Player
- setProxyBypassForLocal 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，setProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984078"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="05f37-106">IWMPNetwork：： setProxyBypassForLocal 方法</span><span class="sxs-lookup"><span data-stu-id="05f37-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="05f37-107">**SetProxyBypassForLocal** 方法會指定如果源伺服器是在區域網路上，是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f37-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f37-108">語法</span><span class="sxs-lookup"><span data-stu-id="05f37-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="05f37-109">參數</span><span class="sxs-lookup"><span data-stu-id="05f37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f37-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f37-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f37-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="05f37-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="05f37-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="05f37-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="05f37-113">*fBypassForLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f37-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f37-114">System.string **值，** 指出是否略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f37-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f37-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="05f37-115">Return value</span></span>

<span data-ttu-id="05f37-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="05f37-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f37-117">備註</span><span class="sxs-lookup"><span data-stu-id="05f37-117">Remarks</span></span>

<span data-ttu-id="05f37-118">除非從 IWMPNetwork 中取出的值為2，否則此方法不會有任何作用，)  (使用手動設定 **。**</span><span class="sxs-lookup"><span data-stu-id="05f37-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="05f37-119">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="05f37-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="05f37-120">範例</span><span class="sxs-lookup"><span data-stu-id="05f37-120">Examples</span></span>

<span data-ttu-id="05f37-121">下列程式碼範例會使用 **setProxyBypassForLocal** ，指定在使用 MMS 通訊協定時，如果源伺服器是在區域網路上，是否略過 Windows Media Player 的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f37-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="05f37-122">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="05f37-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="05f37-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f37-123">Requirements</span></span>



| <span data-ttu-id="05f37-124">需求</span><span class="sxs-lookup"><span data-stu-id="05f37-124">Requirement</span></span> | <span data-ttu-id="05f37-125">值</span><span class="sxs-lookup"><span data-stu-id="05f37-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f37-126">版本</span><span class="sxs-lookup"><span data-stu-id="05f37-126">Version</span></span><br/>   | <span data-ttu-id="05f37-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="05f37-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="05f37-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="05f37-128">Namespace</span></span><br/> | <span data-ttu-id="05f37-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="05f37-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="05f37-130">組件</span><span class="sxs-lookup"><span data-stu-id="05f37-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="05f37-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="05f37-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f37-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f37-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f37-133">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="05f37-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05f37-134">**IWMPNetwork. getProxyBypassForLocal (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="05f37-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05f37-135">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="05f37-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





