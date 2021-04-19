---
title: IWMPNetwork setProxyPort 方法
description: SetProxyPort 方法會指定要使用的 proxy 埠。 |IWMPNetwork setProxyPort 方法
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- setProxyPort 方法 Windows Media Player
- setProxyPort 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，setProxyPort 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984815"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="20564-107">IWMPNetwork：： setProxyPort 方法</span><span class="sxs-lookup"><span data-stu-id="20564-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="20564-108">**SetProxyPort** 方法會指定要使用的 proxy 埠。</span><span class="sxs-lookup"><span data-stu-id="20564-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="20564-109">語法</span><span class="sxs-lookup"><span data-stu-id="20564-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="20564-110">參數</span><span class="sxs-lookup"><span data-stu-id="20564-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20564-111">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20564-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20564-112">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="20564-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="20564-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="20564-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="20564-114">*lProxyPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20564-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20564-115">要使用的 proxy 埠的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="20564-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20564-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="20564-116">Return value</span></span>

<span data-ttu-id="20564-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="20564-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20564-118">備註</span><span class="sxs-lookup"><span data-stu-id="20564-118">Remarks</span></span>

<span data-ttu-id="20564-119">除非從 IWMPNetwork 中取出的值為2，否則此方法不會有任何作用，)  (使用手動設定 **。**</span><span class="sxs-lookup"><span data-stu-id="20564-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="20564-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="20564-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="20564-121">範例</span><span class="sxs-lookup"><span data-stu-id="20564-121">Examples</span></span>

<span data-ttu-id="20564-122">下列程式碼範例會使用 **setProxyPort** 來指定 MMS 通訊協定的 Windows Media Player proxy 埠號碼。</span><span class="sxs-lookup"><span data-stu-id="20564-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="20564-123">按一下按鈕時，就會從文字方塊中取出埠號碼。</span><span class="sxs-lookup"><span data-stu-id="20564-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="20564-124">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="20564-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="20564-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="20564-125">Requirements</span></span>



| <span data-ttu-id="20564-126">需求</span><span class="sxs-lookup"><span data-stu-id="20564-126">Requirement</span></span> | <span data-ttu-id="20564-127">值</span><span class="sxs-lookup"><span data-stu-id="20564-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20564-128">版本</span><span class="sxs-lookup"><span data-stu-id="20564-128">Version</span></span><br/>   | <span data-ttu-id="20564-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="20564-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="20564-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="20564-130">Namespace</span></span><br/> | <span data-ttu-id="20564-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="20564-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="20564-132">組件</span><span class="sxs-lookup"><span data-stu-id="20564-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="20564-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="20564-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20564-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20564-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20564-135">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="20564-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="20564-136">**IWMPNetwork. getProxyPort (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="20564-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="20564-137">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="20564-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





