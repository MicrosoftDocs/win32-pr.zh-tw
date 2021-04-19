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
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a>IWMPNetwork：： getProxyExceptionList 方法

**GetProxyExceptionList** 方法會傳回 proxy 例外清單。

## <a name="syntax"></a>語法


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





## <a name="parameters"></a>參數

<dl> <dt>

*bstrProtocol* \[在\]
</dt> <dd>

表示通訊協定名稱的 **system.string** 。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是略過 proxy 伺服器的主機清單（以分號分隔）。 只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。

## <a name="remarks"></a>備註

當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。

\*字元可以用來做為清單專案的萬用字元。 例如， \* .com 會比對 com 網域中的所有主機，而67則 \* 會比對67類別中的所有主機與子網。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

## <a name="examples"></a>範例

下列程式碼範例會使用 **getProxyExceptionList** 來顯示是否將 Windows Media Player 設定為略過本機位址的 proxy 伺服器。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


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





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyExceptionList (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





