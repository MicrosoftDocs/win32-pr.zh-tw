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
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a>IWMPNetwork：： getProxyBypassForLocal 方法

**GetProxyBypassForLocal** 方法會傳回值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。

## <a name="syntax"></a>語法


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





## <a name="parameters"></a>參數

<dl> <dt>

*bstrProtocol* 
</dt> <dd>

表示通訊協定名稱的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

System.string **值，** 指出是否略過 proxy 伺服器。 只有當 **IWMPNetwork** 傳回的值為 2 (使用手動設定) 時，此值才有意義。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

## <a name="examples"></a>範例

下列程式碼範例會使用 **getProxyBypassForLocal** 來顯示是否將 Windows Media Player 設定為略過本機位址的 proxy 伺服器。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


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





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|-----------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                             |
| 命名空間<br/> | **WMPLib**<br/>                                                                         |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyBypassForLocal (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





