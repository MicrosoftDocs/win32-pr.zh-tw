---
title: User_marshal 屬性
description: '\ 使用者 \_ 封送處理 \ 屬性是 ACF 類型的屬性，類似于以 \ 表示的語法 \_ 。'
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- 遠端程序呼叫 RPC、屬性、user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0501cfd3199d41a49da7f54919c86f9332ce976f33963f23c63a7938338da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923528"
---
# <a name="the-user_marshal-attribute"></a>使用者 \_ 封送處理屬性

\[[使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理 \] 屬性是 ACF 類型的屬性，類似于用來 \[ [表示 \_ ](/windows/desktop/Midl/represent-as)的語法 \] 。 如同 IDL 屬性（ \[ network [ \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] ），它可提供更有效率的方式，在網路上封送處理資料。 **\[ 使用者 \_ 封送 \]** 處理是 ACF 屬性，可讓您將未知的自訂資料類型封送處理。 每個應用程式特定類型都有對應的可類型，可定義網路標記法。

您的應用程式特定類型可以是簡單、複合或指標類型。 主要限制是型別實例必須有固定且妥善定義的記憶體大小。 如果您的型別實例大小需要變更，請使用指標欄位，而不是符合標準的陣列。 或者，您也可以定義可變更型別的指標。

如同 [ **\[ 有線 \_ 封送 \]** 處理] 屬性，您可以提供用於調整大小、封送處理、封送處理和釋放行程的常式。 下表描述四個使用者提供的常式名稱。 <type>是在 **\[ 使用者 \_ 封送 \]** 處理類型定義中指定的 userm *類型*。



| 常式傳回的值                                                            | Description                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | 在用戶端或伺服器端上進行封送處理之前，先調整 RPC 資料緩衝區的大小。 |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | 將用戶端或伺服器端上的資料封送處理。                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | 拆收用戶端或伺服器端上的資料。                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | 釋放伺服器端的資料。                                        |



 

這些使用者提供的常式是由用戶端或伺服器應用程式，以方向屬性為基礎來提供。

如果參數為 \[ [](/windows/desktop/Midl/in) \] ，則用戶端會傳送至伺服器。 用戶端需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。 伺服器需要 **<type> \_ UserUnmarshal** 和 **<type> \_ UserFree** 函數。

針對 \[ [out](/windows/desktop/Midl/out-idl) \] 參數，伺服器會傳送至用戶端。 當用戶端需要 **<type> \_ UserMarshal** 函式時，伺服器需要 **<type> \_ UserSize** 和 **<type> \_ UserMarshal** 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[有線 \_ 封送處理屬性](the-wire-marshal-attribute.md)
</dt> <dt>

[封送處理使用者封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 