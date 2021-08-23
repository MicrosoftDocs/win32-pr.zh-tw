---
title: SetProxyExceptionList 方法
description: SetProxyExceptionList 方法會指定 proxy 例外清單。 |SetProxyExceptionList 方法
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- setProxyExceptionList 方法 Windows Media Player
- setProxyExceptionList 方法 Windows Media Player，Network 類別
- Network 類別 Windows Media Player，setProxyExceptionList 方法
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647298"
---
# <a name="networksetproxyexceptionlist-method"></a>SetProxyExceptionList 方法

**SetProxyExceptionList** 方法會指定 proxy 例外清單。

## <a name="syntax"></a>語法


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*通訊協定* \[在\]
</dt> <dd>

指定通訊協定名稱的 **字串**。 如需支援的通訊協定清單，請參閱 [支援的通訊協定和檔案類型](supported-protocols-and-file-types.md)。

</dd> <dt>

*清單* \[在\]
</dt> <dd>

**字串** ，指定要略過 proxy 伺服器的主機清單（以分號分隔）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當目標 URL 的主機部分符合清單中的專案時，這是電腦、網域及/或位址的清單，將會略過 proxy 伺服器。

\*字元可以用來做為清單專案的萬用字元。 例如， \* .com 會比對 com 網域中的所有主機，而67則 \* 會比對67類別中的所有主機與子網。

除非 **getProxySettings** 傳回值 2 () 使用手動設定，否則這個方法沒有任何作用。

除非呼叫的應用程式是在本機電腦或內部網路上執行，否則這個方法會失敗。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**setProxyExceptionList** ，指定在使用 MMS 通訊協定時，已略過 proxy 伺服器的主機清單。 新的清單會從 ID = ".XLIST" 的 HTML 文字元素中取出。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
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

 

 





