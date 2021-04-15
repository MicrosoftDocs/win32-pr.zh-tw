---
title: message 屬性
description: '\ Message \ 屬性工作表示遠端程序呼叫會被視為從用戶端到伺服器的訊息。'
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- message 屬性 MIDL
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463056"
---
# <a name="message-attribute"></a>message 屬性

Message 屬性（ **\[ message \]** attribute）指出遠端程序呼叫會被視為從用戶端到伺服器的訊息。

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用-屬性-清單* 
</dt> <dd>

適用于函數的其他屬性。 只有 **\[** [**local**](local.md) **\]** 、 **\[** [**了 nocode**](nocode.md) **\]** 、 **\[** [**code**](code.md) **\]** 和 **\[** [**optimize**](optimize.md) **\]** 屬性可搭配 **\[ message \]** 屬性使用。

</dd> <dt>

*函數名稱* 
</dt> <dd>

IDL 檔案中所定義的函式名稱。

</dd> <dt>

*選擇性-參數-屬性* 
</dt> <dd>

將套用至參數的零或多個 MIDL 屬性。

</dd> <dt>

*參數名稱* 
</dt> <dd>

在 IDL 檔案中定義之參數的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

當用戶端收到來自用戶端的訊息時，會透過 [**ncadg \_ mq**](ncadg-mq.md)訊息佇列傳輸，以非同步方式將 **\[ \] 訊息** 屬性的遠端程序呼叫傳遞至伺服器。 您可以指定 **ncadg \_ mq** 傳輸通訊協定，而不使用 **\[ \] message** 屬性，來指出同步模式的訊息。

藉由指定非同步模式訊息， **\[ message \]** 屬性可讓用戶端進行遠端程序呼叫，並立即傳回，即使伺服器應用程式沒有回應。 如果目標伺服器無法使用，則會儲存呼叫，直到伺服器變成可用為止。

此外，非同步模式的訊息可讓您控制伺服器接收佇列的訊息佇列屬性。 如需有關選取服務品質、呼叫優先順序，以及伺服器進程的呼叫存留期的詳細資訊，請參閱 [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) 。

下列限制也適用于 **\[ message \]** 屬性：

-   Microsoft Message Queuing 必須在用戶端和伺服器系統中執行，而且這些系統必須由訊息佇列安裝範圍所判斷，彼此都可以看見。
-   系結必須使用已知的端點和 [**ncadg \_ mq**](ncadg-mq.md) 傳輸通訊協定。
-   函數不能包含 output 參數或 [**void**](void.md)以外的傳回型別。 請注意，後者的限制會讓 **\[ 訊息 \]** 屬性不適合 COM (物件) 介面方法。 下一版的 MIDL 將允許 **\[ 訊息 \]** 函數傳回錯誤 \_ 狀態 \_ t 或 HRESULT。
-   至少包含一個 **\[ 訊息 \]** 呼叫的任何介面，都必須先呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)或 [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex)來註冊，然後再呼叫 [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex)。 否則，在註冊介面之前，在佇列中等候伺服器的呼叫會被讀取，且呼叫會失敗。

## <a name="examples"></a>範例

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**代碼**](code.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**ncadg \_ mq**](ncadg-mq.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> <dt>

[**優化**](optimize.md)
</dt> <dt>

[RPC 訊息佇列](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 