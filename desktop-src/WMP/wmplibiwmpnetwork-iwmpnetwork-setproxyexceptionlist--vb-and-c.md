---
title: IWMPNetwork setProxyExceptionList 方法
description: SetProxyExceptionList 方法會指定 proxy 例外清單。 |IWMPNetwork setProxyExceptionList 方法
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- setProxyExceptionList 方法 Windows Media Player
- setProxyExceptionList 方法 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，setProxyExceptionList 方法
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991263"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="c0603-107">IWMPNetwork：： setProxyExceptionList 方法</span><span class="sxs-lookup"><span data-stu-id="c0603-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="c0603-108">**SetProxyExceptionList** 方法會指定 proxy 例外清單。</span><span class="sxs-lookup"><span data-stu-id="c0603-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0603-109">語法</span><span class="sxs-lookup"><span data-stu-id="c0603-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="c0603-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0603-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0603-111">*bstrProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0603-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0603-112">表示通訊協定名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="c0603-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="c0603-113">如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c0603-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0603-114">*pbstrExceptionList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0603-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0603-115">**System.string** ，這是略過 proxy 伺服器的主機清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c0603-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="c0603-116">開頭和尾端空格不應該存在。</span><span class="sxs-lookup"><span data-stu-id="c0603-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0603-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0603-117">Return value</span></span>

<span data-ttu-id="c0603-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c0603-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0603-119">備註</span><span class="sxs-lookup"><span data-stu-id="c0603-119">Remarks</span></span>

<span data-ttu-id="c0603-120">當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c0603-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="c0603-121">\*字元可以用來做為清單專案的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c0603-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="c0603-122">例如， \* .com 會比對 com 網域中的所有主機，而67則 \* 會比對67類別中的所有主機與子網。</span><span class="sxs-lookup"><span data-stu-id="c0603-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="c0603-123">除非從 IWMPNetwork 中取出的值為2，否則此方法不會有任何作用，)  (使用手動設定 **。**</span><span class="sxs-lookup"><span data-stu-id="c0603-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="c0603-124">除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="c0603-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="c0603-125">範例</span><span class="sxs-lookup"><span data-stu-id="c0603-125">Examples</span></span>

<span data-ttu-id="c0603-126">下列程式碼範例會使用 **setProxyExceptionList** 來指定在使用 MMS 通訊協定時略過 proxy 伺服器的主機清單。</span><span class="sxs-lookup"><span data-stu-id="c0603-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="c0603-127">按一下按鈕時，就會從文字方塊中取出新的清單。</span><span class="sxs-lookup"><span data-stu-id="c0603-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="c0603-128">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="c0603-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c0603-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0603-129">Requirements</span></span>



| <span data-ttu-id="c0603-130">需求</span><span class="sxs-lookup"><span data-stu-id="c0603-130">Requirement</span></span> | <span data-ttu-id="c0603-131">值</span><span class="sxs-lookup"><span data-stu-id="c0603-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0603-132">版本</span><span class="sxs-lookup"><span data-stu-id="c0603-132">Version</span></span><br/>   | <span data-ttu-id="c0603-133">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="c0603-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c0603-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0603-134">Namespace</span></span><br/> | <span data-ttu-id="c0603-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c0603-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c0603-136">組件</span><span class="sxs-lookup"><span data-stu-id="c0603-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c0603-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c0603-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0603-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0603-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0603-139">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c0603-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c0603-140">**IWMPNetwork. getProxyExceptionList (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c0603-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c0603-141">**IWMPNetwork. getProxySettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c0603-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





