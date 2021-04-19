---
title: IsAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986047"
---
# <a name="dvdisavailable"></a>IsAvailable

**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>參數

*name*

包含下列其中一個值的 **字串**。



| String     | Description                                                                            |
|------------|----------------------------------------------------------------------------------------|
| 上一步       | 判斷 **back** 方法是否可用。                                   |
| Dvd        | 判斷是否已載入 DVD。                                                  |
| dvdDecoder | 判斷系統上是否已安裝 DVD 解碼器。                             |
| resume     | 判斷 **resume** 方法是否可用。                                 |
| titleMenu  | 判斷 **titleMenu** 方法是否可用。                              |
| topMenu    | 判斷 **topMenu** 方法是否可用。 通常稱為根功能表。 |



 

## <a name="return-values"></a>傳回值

這個方法會傳回唯讀的 **布林值** ，指出指定的參數是否可用。

## <a name="remarks"></a>備註

Windows Media Player 的 DVD 功能將無法在未安裝協力廠商 DVD 解碼器的電腦上運作。 您可以藉由呼叫 **isAvailable** ( "dvdDecoder" ) 來判斷是否有可用的解碼器。

每個 DVD 的撰寫方式不同。 DVD 播放和流覽期間可用的方法取決於 DVD 的編寫方式。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 版本<br/>                  | 適用于 Windows XP 或更新版本的 Windows Media Player<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DVD 物件**](dvd-object.md)
</dt> </dl>

 

 





