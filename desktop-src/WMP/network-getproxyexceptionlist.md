---
title: GetProxyExceptionList 方法
description: GetProxyExceptionList 方法會抓取 proxy 例外清單。
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- getProxyExceptionList 方法 Windows Media Player
- getProxyExceptionList 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxyExceptionList 方法
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976214"
---
# <a name="networkgetproxyexceptionlist-method"></a>GetProxyExceptionList 方法

**GetProxyExceptionList** 方法會抓取 proxy 例外清單。

## <a name="syntax"></a>語法


```JScript
strRetVal = Network.getProxyExceptionList(
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

這個方法會傳回 **字串** ，指定要略過 proxy 伺服器的主機清單（以分號分隔）。 只有當 **getProxySettings** 傳回兩個 (使用手動設定) 的值時，傳回的值才有意義。

## <a name="remarks"></a>備註

當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。

\*字元可以用來做為清單專案的萬用字元。 例如， \* .com 會比對 com 網域中的所有主機（67）。 \* 會比對67類別中的所有主機與子網。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**getProxyExceptionList** 可顯示 MMS 和 HTTP 通訊協定的已略過 proxy 清單。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

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

 

 





