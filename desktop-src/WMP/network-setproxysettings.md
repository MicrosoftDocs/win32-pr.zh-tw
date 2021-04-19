---
title: SetProxySettings 方法
description: SetProxySettings 方法會為指定的通訊協定指定 proxy 設定。
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- setProxySettings 方法 Windows Media Player
- setProxySettings 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxySettings 方法
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984292"
---
# <a name="networksetproxysettings-method"></a>SetProxySettings 方法

**SetProxySettings** 方法會為指定的通訊協定指定 proxy 設定。

## <a name="syntax"></a>語法


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*設定* \[在\]
</dt> <dd>

包含下列其中一個值的 (**long**) **數位**。



| 值 | 描述                                                          |
|-------|----------------------------------------------------------------------|
| 0     | 不使用 Proxy 伺服器：                                           |
| 1     | 使用目前瀏覽器的 proxy 設定 (僅適用于 HTTP) 。 |
| 2     | 使用手動指定的 proxy 設定。                           |
| 3     | 自動偵測 proxy 設定。                                      |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列範例會使用 JScript 搭配 HTML SELECT **元素，以允許使用者指定 HTTP 通訊協定的 Windows Media Player proxy 設定。** 使用 ID = "player" 建立 player 物件。


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

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

 

 





