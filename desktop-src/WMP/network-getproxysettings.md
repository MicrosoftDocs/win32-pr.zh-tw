---
title: GetProxySettings 方法
description: GetProxySettings 方法會取得指定之通訊協定的 proxy 設定。
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- getProxySettings 方法 Windows Media Player
- getProxySettings 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，getProxySettings 方法
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647438"
---
# <a name="networkgetproxysettings-method"></a>GetProxySettings 方法

**GetProxySettings** 方法會取得指定之通訊協定的 proxy 設定。

## <a name="syntax"></a>語法


```JScript
retVal = Network.getProxySettings(
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

這個方法會傳回 **數位** (**Long**) ，其中包含下列其中一個值。



| 值 | 描述                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | 未使用 proxy 伺服器。                                                |
| 1     | 目前瀏覽器的 proxy 設定正在使用中 (僅適用于 HTTP) 。 |
| 2     | 正在使用手動指定的 proxy 設定。                            |
| 3     | 系統會自動偵測到 proxy 設定。                                      |



 

## <a name="remarks"></a>備註

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**getProxySettings** 顯示一則訊息，它會在瀏覽器視窗中提供播放程式目前 proxy 設定的相關資訊。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

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

 

 





