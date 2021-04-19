---
title: GetProxyPort 方法
description: GetProxyPort 方法會抓取正在使用的 proxy 埠。
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- getProxyPort 方法 Windows Media Player
- getProxyPort 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyPort 方法
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995672"
---
# <a name="networkgetproxyport-method"></a>GetProxyPort 方法

**GetProxyPort** 方法會抓取正在使用的 proxy 埠。

## <a name="syntax"></a>語法


```JScript
retVal = Network.getProxyPort(
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

這個方法會傳回 **數位** (**Long**) ，其中包含所使用的 proxy 埠。 只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**getProxyPort** 可顯示 MMS 和 HTTP 通訊協定的目前 Windows Media Player proxy 埠號碼。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

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

 

 





