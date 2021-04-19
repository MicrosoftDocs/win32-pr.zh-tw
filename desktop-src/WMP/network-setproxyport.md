---
title: SetProxyPort 方法
description: SetProxyPort 方法會指定要使用的 proxy 埠。 |SetProxyPort 方法
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- setProxyPort 方法 Windows Media Player
- setProxyPort 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyPort 方法
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993940"
---
# <a name="networksetproxyport-method"></a>SetProxyPort 方法

**SetProxyPort** 方法會指定要使用的 proxy 埠。

## <a name="syntax"></a>語法


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*埠* \[在\]
</dt> <dd>

 (**long**) 指定要使用的 Proxy 埠 **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**setProxyPort** 指定 MMS 通訊協定的 Windows Media Player proxy 埠號碼。 埠號碼是從 ID = "PORT" 的 HTML INPUT 元素取出。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
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

 

 





