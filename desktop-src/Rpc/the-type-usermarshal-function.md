---
title: Type_UserMarshal 函式
description: 型 \_ 別 UserMarshal 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382785"
---
# <a name="the-type_usermarshal-function"></a>型別 \_ UserMarshal 函式

**<type> \_ UserMarshal** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。 Stub 會呼叫這個函式，以在用戶端或伺服器端上封送處理資料。 函式定義如下：

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

函 <type> 式名稱中的，表示在 **\[ 有線 \_ 封送 \]** 處理或 **\[ 使用者 \_ 封 \] 送** 處理類型定義中指定的 userm 類型。 此類型可以是 untransmittable 或甚至是在與 **\[ 使用者 \_ 封送 \]** 處理屬性搭配使用時，也就是 MIDL 編譯器的未知類型。 在函式原型中未使用 transmissible 類型) 名稱 (網路類型名稱。 不過，請注意，網路類型會定義憑證 DCE 所指定之資料的網路版面配置。

*PFlags* 參數是不帶正負號的長旗標欄位的指標。 旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。 下方的單字包含由 COM 通道所定義的封送處理內容旗標。 欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。

*PBuffer* 參數是目前的緩衝區指標。 此指標不一定會在輸入時對齊。 您的 **<type> \_ UserMarshal** 函式應適當地對齊緩衝區指標、封送處理資料，並傳回新的緩衝區位置，也就是封送處理物件之後第一個位元組的位址。 請記住，網路類型規格會決定緩衝區中資料的實際版面配置。

*PMyObj* 參數是使用者類型物件的指標。

傳回值是新的緩衝區位置，也就是取消封送處理物件之後第一個位元組的位址。

當您不正確地計算資料的大小，並嘗試封送處理超過預期的資料時，可能會發生緩衝區溢位。 請小心避免此情況。 您可以使用 **<type> \_ UserMarshal** 傳回的指標來檢查它。 否則，您之後可能會有 NDR 引擎引發緩衝區溢位例外狀況的風險。

必須在本機攔截和處理例外狀況，不能允許例外狀況 propigated 呼叫堆疊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封送處理使用者 \_ 封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 