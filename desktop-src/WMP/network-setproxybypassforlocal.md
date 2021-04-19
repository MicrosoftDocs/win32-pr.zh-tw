---
title: SetProxyBypassForLocal 方法
description: SetProxyBypassForLocal 方法會指定一個值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- setProxyBypassForLocal 方法 Windows Media Player
- setProxyBypassForLocal 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyBypassForLocal 方法
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984088"
---
# <a name="networksetproxybypassforlocal-method"></a>SetProxyBypassForLocal 方法

**SetProxyBypassForLocal** 方法會指定一個值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。

## <a name="syntax"></a>語法


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*略過* \[在\]
</dt> <dd>

**布林值** ，指定是否略過 proxy 伺服器。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。如果源伺服器是在區域網路上，則使用 **setProxyBypassForLocal** 來指定是否略過 Windows Media Player 的 proxy 伺服器。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> </dl>

 

 





