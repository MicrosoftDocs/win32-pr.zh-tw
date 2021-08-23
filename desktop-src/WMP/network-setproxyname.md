---
title: SetProxyName 方法
description: SetProxyName 方法會指定要使用的 proxy 伺服器名稱。 |SetProxyName 方法
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- setProxyName 方法 Windows Media Player
- setProxyName 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyName 方法
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134921"
---
# <a name="networksetproxyname-method"></a>SetProxyName 方法

**SetProxyName** 方法會指定要使用的 proxy 伺服器名稱。

## <a name="syntax"></a>語法


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

**字串** ，指定要使用的 proxy 伺服器名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**setProxyName** 指定 MMS 通訊協定 Windows Media Player proxy 伺服器的名稱。 新名稱會從 ID = "NAME" 的 HTML 文字元素中取出。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
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

 

 





