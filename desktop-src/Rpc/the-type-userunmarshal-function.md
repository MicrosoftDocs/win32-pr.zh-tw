---
title: Type_UserUnmarshal 函式
description: 型 \_ 別 UserUnmarshal 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05281e7ae9d25ee25b4e3198dd834c78d81c3f53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884152"
---
# <a name="the-type_userunmarshal-function"></a>型別 \_ UserUnmarshal 函式

**&lt; 型別 &gt; \_ UserUnmarshal** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。 Stub 會呼叫這個函式來 unmarshal 用戶端或伺服器端上的資料。 函式定義如下：

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

函 &lt; &gt; 式名稱中的型別表示在 **\[ 有線 \_ 封 \] 送** 處理或 **\[ 使用者 \_ \] 封送** 處理類型定義中指定的 userm 類型。 這種類型在與 **\[ 使用者 \_ 封送 \]** 處理屬性（attribute）搭配使用時，可能是 UNTRANSMITTABLE 或甚至是： MIDL 編譯器的未知。 在函式原型中未使用 transmissible 類型) 名稱 (網路類型名稱。 不過，請注意，網路類型會定義憑證 DCE 所指定之資料的網路版面配置。

*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。 旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。 下方的單字包含由 COM 通道所定義的封送處理內容旗標。 欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。

*PBuffer* 參數是目前的緩衝區指標。 此指標不一定會在輸入時對齊。 您的 **&lt; 型別 &gt; \_ UserUnmarshal** 函式應適當地對齊緩衝區指標，unmarshal 資料，並傳回新的緩衝區位置，也就是取消封送處理物件之後第一個位元組的位址。

*PMyObj* 參數是使用者定義型別物件的指標。

在異類環境中，NDR 引擎會在呼叫 **&lt; 型別 &gt; \_ UserUnmarshal** 函式之前，先執行任何必要的資料轉換。 請注意，「NDR 引擎」會根據針對此使用者資料類型所提供的網路類型定義來執行此資料轉換。 旗標表示寄件者的資料標記法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封送處理使用者 \_ 封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
