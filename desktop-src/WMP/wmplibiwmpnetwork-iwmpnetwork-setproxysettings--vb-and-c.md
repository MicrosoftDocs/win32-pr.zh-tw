---
title: IWMPNetwork setProxySettings 方法
description: SetProxySettings 方法會指定通訊協定的 proxy 設定。
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- setProxySettings 方法 Windows Media Player
- setProxySettings 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，setProxySettings 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990853"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="99998-106">IWMPNetwork：： setProxySettings 方法</span><span class="sxs-lookup"><span data-stu-id="99998-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="99998-107">**SetProxySettings** 方法會指定通訊協定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="99998-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="99998-108">語法</span><span class="sxs-lookup"><span data-stu-id="99998-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="99998-109">參數</span><span class="sxs-lookup"><span data-stu-id="99998-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99998-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99998-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99998-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="99998-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="99998-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="99998-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="99998-113">*lProxySetting* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99998-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99998-114">屬於下列其中一個值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="99998-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="99998-115">值</span><span class="sxs-lookup"><span data-stu-id="99998-115">Value</span></span> | <span data-ttu-id="99998-116">描述</span><span class="sxs-lookup"><span data-stu-id="99998-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="99998-117">0</span><span class="sxs-lookup"><span data-stu-id="99998-117">0</span></span>     | <span data-ttu-id="99998-118">不使用 Proxy 伺服器：</span><span class="sxs-lookup"><span data-stu-id="99998-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="99998-119">1</span><span class="sxs-lookup"><span data-stu-id="99998-119">1</span></span>     | <span data-ttu-id="99998-120">使用目前瀏覽器的 proxy 設定 (僅適用于 HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="99998-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="99998-121">2</span><span class="sxs-lookup"><span data-stu-id="99998-121">2</span></span>     | <span data-ttu-id="99998-122">使用手動指定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="99998-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="99998-123">3</span><span class="sxs-lookup"><span data-stu-id="99998-123">3</span></span>     | <span data-ttu-id="99998-124">自動偵測 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="99998-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99998-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="99998-125">Return value</span></span>

<span data-ttu-id="99998-126">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="99998-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99998-127">備註</span><span class="sxs-lookup"><span data-stu-id="99998-127">Remarks</span></span>

<span data-ttu-id="99998-128">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="99998-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="99998-129">範例</span><span class="sxs-lookup"><span data-stu-id="99998-129">Examples</span></span>

<span data-ttu-id="99998-130">下列程式碼範例會使用清單方塊，讓使用者能夠設定 HTTP 通訊協定的 Windows Media Player proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="99998-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="99998-131">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="99998-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="99998-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="99998-132">Requirements</span></span>



| <span data-ttu-id="99998-133">需求</span><span class="sxs-lookup"><span data-stu-id="99998-133">Requirement</span></span> | <span data-ttu-id="99998-134">值</span><span class="sxs-lookup"><span data-stu-id="99998-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99998-135">版本</span><span class="sxs-lookup"><span data-stu-id="99998-135">Version</span></span><br/>   | <span data-ttu-id="99998-136">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="99998-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="99998-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="99998-137">Namespace</span></span><br/> | <span data-ttu-id="99998-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="99998-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="99998-139">組件</span><span class="sxs-lookup"><span data-stu-id="99998-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="99998-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="99998-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99998-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99998-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99998-142">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="99998-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="99998-143">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="99998-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





