---
title: IWMPNetwork setProxyName 方法
description: SetProxyName 方法會指定要使用的 proxy 伺服器名稱。 |IWMPNetwork setProxyName 方法
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- setProxyName 方法 Windows Media Player
- setProxyName 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，setProxyName 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001032"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="b3009-107">IWMPNetwork：： setProxyName 方法</span><span class="sxs-lookup"><span data-stu-id="b3009-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="b3009-108">**SetProxyName** 方法會指定要使用的 proxy 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b3009-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3009-109">語法</span><span class="sxs-lookup"><span data-stu-id="b3009-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="b3009-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3009-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3009-111">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3009-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3009-112">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="b3009-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="b3009-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b3009-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3009-114">*bstrProxyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3009-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3009-115">**System.string** ，這是要使用之 proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3009-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3009-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3009-116">Return value</span></span>

<span data-ttu-id="b3009-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3009-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3009-118">備註</span><span class="sxs-lookup"><span data-stu-id="b3009-118">Remarks</span></span>

<span data-ttu-id="b3009-119">除非從 IWMPNetwork 中取出的值為2，否則此方法不會有任何作用，)  (使用手動設定 **。**</span><span class="sxs-lookup"><span data-stu-id="b3009-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="b3009-120">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="b3009-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="b3009-121">範例</span><span class="sxs-lookup"><span data-stu-id="b3009-121">Examples</span></span>

<span data-ttu-id="b3009-122">下列程式碼範例會使用 **setProxyName** 來指定 MMS 通訊協定 Windows Media Player proxy 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3009-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="b3009-123">按一下按鈕時，就會從文字方塊中取出新的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3009-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="b3009-124">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b3009-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b3009-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3009-125">Requirements</span></span>



| <span data-ttu-id="b3009-126">需求</span><span class="sxs-lookup"><span data-stu-id="b3009-126">Requirement</span></span> | <span data-ttu-id="b3009-127">值</span><span class="sxs-lookup"><span data-stu-id="b3009-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3009-128">版本</span><span class="sxs-lookup"><span data-stu-id="b3009-128">Version</span></span><br/>   | <span data-ttu-id="b3009-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b3009-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b3009-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3009-130">Namespace</span></span><br/> | <span data-ttu-id="b3009-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b3009-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b3009-132">組件</span><span class="sxs-lookup"><span data-stu-id="b3009-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b3009-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b3009-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3009-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3009-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3009-135">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b3009-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3009-136">**IWMPNetwork. getProxyName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b3009-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3009-137">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b3009-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





