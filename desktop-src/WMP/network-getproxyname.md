---
title: GetProxyName 方法
description: GetProxyName 方法會抓取正在使用之 proxy 伺服器的名稱。
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- getProxyName 方法 Windows Media Player
- getProxyName 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyName 方法
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f40eb7eb695376768cd8168e1eb1d1916c8e84e6ede8ef93251df6097a15d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647448"
---
# <a name="networkgetproxyname-method"></a>GetProxyName 方法

**GetProxyName** 方法會抓取正在使用之 proxy 伺服器的名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = Network.getProxyName(
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

這個方法會傳回 **字串** ，其中包含所使用之 proxy 伺服器的名稱。 只有當 **getProxySettings** 傳回的值為 2 () 使用手動設定時，傳回的值才有意義。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**getProxyName** ，顯示 HTTP 和 MMS 通訊協定的 Windows Media Player proxy 伺服器名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

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

 

 





