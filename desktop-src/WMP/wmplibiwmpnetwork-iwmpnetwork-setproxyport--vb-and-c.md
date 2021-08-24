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
ms.openlocfilehash: 7e79453ee2d69a0c6b227006416e49b4d4c24b99b3b02dd2bd00cd3bafafc5b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734838"
---
# <a name="iwmpnetworksetproxyport-method"></a>IWMPNetwork：： setProxyPort 方法

**SetProxyPort** 方法會指定要使用的 proxy 埠。

## <a name="syntax"></a>語法


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





## <a name="parameters"></a>參數

<dl> <dt>

*bstrProtocol* \[在\]
</dt> <dd>

表示通訊協定名稱的 **system.string** 。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*lProxyPort* \[在\]
</dt> <dd>

要使用的 proxy 埠的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非從 IWMPNetwork 中取出的值為2，否則此方法不會有任何作用，)  (使用手動設定 **。**

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

## <a name="examples"></a>範例

下列程式碼範例會使用 **setProxyPort** 來指定 MMS 通訊協定的 Windows Media Player proxy 埠號碼。 按一下按鈕時，就會從文字方塊中取出埠號碼。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


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

[**IWMPNetwork. getProxyPort (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





