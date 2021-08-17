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
ms.openlocfilehash: 2e5c8c15df5e741c02bf3c47ecac8b3f57d4adddfeeb41cb6a71cf418b600006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745936"
---
# <a name="iwmpnetworkgetproxyname-method"></a>IWMPNetwork：： getProxyName 方法

**GetProxyName** 方法會傳回所使用 proxy 伺服器的名稱。

## <a name="syntax"></a>語法


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





## <a name="parameters"></a>參數

<dl> <dt>

*bstrProtocol* \[在\]
</dt> <dd>

表示通訊協定名稱的 **system.string** 。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是所使用之 proxy 伺服器的名稱。 只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

## <a name="examples"></a>範例

下列程式碼範例會使用 **getProxyName** 來顯示 HTTP 和 MMS 通訊協定的 Windows Media Player proxy 伺服器名稱。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


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

[**IWMPNetwork. setProxyName (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





