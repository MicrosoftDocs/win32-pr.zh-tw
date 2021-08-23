---
title: GetProxyBypassForLocal 方法
description: GetProxyBypassForLocal 方法會抓取值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- getProxyBypassForLocal 方法 Windows Media Player
- getProxyBypassForLocal 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f22eb6187938318d95b9dd7a473b58e216315210d4af41c29b352b2654cbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054556"
---
# <a name="networkgetproxybypassforlocal-method"></a>GetProxyBypassForLocal 方法

**GetProxyBypassForLocal** 方法會抓取值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。

## <a name="syntax"></a>語法


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值** ，指出是否略過 proxy 伺服器。 只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**getProxyBypassForLocal** 顯示 Windows Media Player 是否設定為略過本機位址的 proxy 伺服器。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> <dt>

[**GetProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





