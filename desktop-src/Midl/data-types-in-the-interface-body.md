---
title: 介面主體中的資料類型
description: 介面主體（以大括弧 ( ) 括住）包含將在遠端程序呼叫中使用的資料類型，以及將從遠端執行之函式的原型。
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- 介面 MIDL、資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6691ccf89e1bff3b0e980678a30c6f706b724e4f30192d7960183c00cc00c237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979707"
---
# <a name="data-types-in-the-interface-body"></a>介面主體中的資料類型

介面主體（以大括弧 ( {} ) 括住）包含將在遠端程序呼叫中使用的資料類型，以及將從遠端執行之函式的原型。 介面主體可以包含 imports、pragma、常數宣告、型別宣告和函式宣告。 除了在憑證相容性模式中，MIDL 編譯器也允許變數定義形式的隱含宣告。

請注意，RPC 介面的憑證-DCE 規格不允許單一 IDL 檔案中有多個介面。 因此，如果您要在 MIDL 的憑證相容性模式中進行編譯 ( [**/osf**](-osf.md)) ，您的 IDL 檔案只能包含一個介面。

如需使用 MIDL 編譯器來產生類型程式庫的詳細資訊，請參閱使用 [Midl 產生類型程式庫](generating-a-type-library-with-midl-2.md)。

在 Microsoft RPC 中，IDL 檔案可以包含多個介面，且這些介面可在定義) 的 IDL 檔案內 (向前宣告。 例如：

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




