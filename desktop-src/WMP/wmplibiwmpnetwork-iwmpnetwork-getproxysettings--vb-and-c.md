---
title: IWMPNetwork getProxySettings 方法
description: GetProxySettings 方法會傳回通訊協定的 proxy 設定相關資訊。
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- getProxySettings 方法 Windows Media Player
- getProxySettings 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，getProxySettings 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996193"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="e03f6-106">IWMPNetwork：： getProxySettings 方法</span><span class="sxs-lookup"><span data-stu-id="e03f6-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="e03f6-107">**GetProxySettings** 方法會傳回通訊協定的 proxy 設定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e03f6-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="e03f6-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="e03f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="e03f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e03f6-110">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e03f6-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e03f6-111">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="e03f6-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="e03f6-112">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="e03f6-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e03f6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e03f6-113">Return value</span></span>

<span data-ttu-id="e03f6-114">屬於下列其中一個值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="e03f6-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="e03f6-115">值</span><span class="sxs-lookup"><span data-stu-id="e03f6-115">Value</span></span> | <span data-ttu-id="e03f6-116">描述</span><span class="sxs-lookup"><span data-stu-id="e03f6-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e03f6-117">0</span><span class="sxs-lookup"><span data-stu-id="e03f6-117">0</span></span>     | <span data-ttu-id="e03f6-118">未使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e03f6-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="e03f6-119">1</span><span class="sxs-lookup"><span data-stu-id="e03f6-119">1</span></span>     | <span data-ttu-id="e03f6-120">目前瀏覽器的 proxy 設定正在使用 (僅適用于 HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="e03f6-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="e03f6-121">2</span><span class="sxs-lookup"><span data-stu-id="e03f6-121">2</span></span>     | <span data-ttu-id="e03f6-122">正在使用手動指定的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="e03f6-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="e03f6-123">3</span><span class="sxs-lookup"><span data-stu-id="e03f6-123">3</span></span>     | <span data-ttu-id="e03f6-124">系統會自動偵測到 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="e03f6-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="e03f6-125">備註</span><span class="sxs-lookup"><span data-stu-id="e03f6-125">Remarks</span></span>

<span data-ttu-id="e03f6-126">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="e03f6-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="e03f6-127">範例</span><span class="sxs-lookup"><span data-stu-id="e03f6-127">Examples</span></span>

<span data-ttu-id="e03f6-128">下列程式碼範例會使用 **getProxySettings** 來顯示訊息，此訊息會提供標籤中有關播放程式目前 proxy 設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="e03f6-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="e03f6-129">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="e03f6-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="e03f6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e03f6-130">Requirements</span></span>



| <span data-ttu-id="e03f6-131">需求</span><span class="sxs-lookup"><span data-stu-id="e03f6-131">Requirement</span></span> | <span data-ttu-id="e03f6-132">值</span><span class="sxs-lookup"><span data-stu-id="e03f6-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03f6-133">版本</span><span class="sxs-lookup"><span data-stu-id="e03f6-133">Version</span></span><br/>   | <span data-ttu-id="e03f6-134">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e03f6-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e03f6-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="e03f6-135">Namespace</span></span><br/> | <span data-ttu-id="e03f6-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e03f6-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e03f6-137">組件</span><span class="sxs-lookup"><span data-stu-id="e03f6-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e03f6-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e03f6-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03f6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e03f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03f6-140">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e03f6-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e03f6-141">**IWMPNetwork. setProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e03f6-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





