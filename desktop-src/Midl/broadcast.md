---
title: 廣播屬性
description: 關鍵字 \ 廣播 \ 指定將遠端程序呼叫傳送至區域網路上的所有伺服器。
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- 廣播屬性 MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f176b03f9d33ee1bbe1d0e805dfc109de477b7499f8fd624ba7732709dc61a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385234"
---
# <a name="broadcast-attribute"></a>廣播屬性

關鍵字 **\[ 廣播 \]** 指定將遠端程序呼叫傳送至區域網路上的所有伺服器。

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的零或多個 IDL 屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定要套用至函數的其他屬性。 以逗號分隔多個屬性。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定將套用 **\[ 廣播 \]** 屬性的函式名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 廣播 \]** 關鍵字指定常式一律會廣播到網路上的所有伺服器，而不是傳遞至一部特定的伺服器。用戶端會接收第一個回復的輸出以成功傳回，而後續回復則會捨棄。

具有 **\[ 廣播 \]** 屬性的作業會隱含為 [**\[ 等冪 \]**](idempotent.md)運算。 但是， **\[ 廣播 \]** 屬性會指定具有 **\[ 等冪 \]** 屬性之函式沒有的其他屬性。 具體而言，使用 [ **\[ 廣播 \]** ] 屬性的函式會指定在一個遠端程序呼叫的結果中，可以多次呼叫常式。 同時，可以將它們傳送至多部伺服器。 這與 **\[ 等冪 \]** 屬性不同，它只會指定當呼叫未完成時，可以重試呼叫。

如果遠端程式將它的呼叫廣播到區域網路上的所有主機，則必須使用 [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md) 或 [**ncadg \_ ipx**](ncadg-ipx.md) 通訊協定順序。 請注意， **\[ 廣播 \]** 封包的大小取決於使用中的資料包服務。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**也許**](maybe.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> </dl>

 

 




