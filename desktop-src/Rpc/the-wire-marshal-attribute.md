---
title: Wire_marshal 屬性
description: '\\ 傳址 \_ 封送處理 \ 屬性是類似于 \ 傳輸形式的 IDL 型別屬性 \_ （attribute），但提供更有效率的方式，在網路上封送處理資料。'
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- 遠端程序呼叫 RPC、屬性、wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376105"
---
# <a name="the-wire_marshal-attribute"></a>有線 \_ 封送處理屬性

[ \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理] \] 屬性是一種 IDL 型別屬性，類似于 \[ [傳輸 \_ ](/windows/desktop/Midl/transmit-as)的語法 \] ，但是提供更有效率的方式在網路上封送處理資料。

您可以使用 [ \[ **有線 \_ 封送** 處理] \] 屬性來指定要傳送的資料類型，以取代應用程式特定的資料類型。 每個應用程式特定類型都有對應的可類型，可定義網路) 上所用標記法 (的網路標記法。應用程式專屬的型別不需要可，但必須是 MIDL 可識別的型別。 若要將未知的類型封送處理為 MIDL，請使用 ACF 屬性 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理 \] 。

您的應用程式特定類型可以是簡單、複合或指標類型。 主要限制是型別實例必須有固定且妥善定義的記憶體大小。 如果您的型別實例大小需要變更，請使用指標欄位，而不是符合標準的陣列。 或者，您也可以定義可變更型別的指標。

您必須提供用來調整大小、封送處理和封送處理資料的常式，以及釋放相關聯的記憶體。 下表描述四個使用者提供的常式名稱。 <type>是在 \[ **有線 \_ 封送** 處理類型定義中指定的 userm 類型 \] 。



| 常式傳回的值                                                            | Description                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | 在用戶端或伺服器端上進行封送處理之前，先調整 RPC 資料緩衝區的大小。 |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | 將用戶端或伺服器端上的資料封送處理。                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | 拆收用戶端或伺服器端上的資料。                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | 釋放伺服器端的資料。                                        |



 

這些程式設計人員提供的常式是由用戶端或伺服器應用程式根據方向屬性提供。

如果參數為 \[ [](/windows/desktop/Midl/in) \] ，則用戶端會傳送至伺服器。 用戶端需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。 伺服器需要 **<type> \_ UserUnmarshal** 和 **<type> \_ UserFree** 函數。

針對 \[ [out](/windows/desktop/Midl/out-idl) \] 參數，伺服器會傳送至用戶端。 當用戶端需要 **<type> \_ UserMarshal** 函式時，伺服器需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用者 \_ 封送處理屬性](the-user-marshal-attribute.md)
</dt> <dt>

[封送處理使用者 \_ 封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 