---
title: 類型序列化
description: MIDL 編譯器會針對套用 \ 編碼 \ 或 \ 解碼 \ 屬性的每個類型，最多產生三個函數。
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674617bc98c92dbc684a29d1a3c91ac6a7429e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092903"
---
# <a name="type-serialization"></a>類型序列化

MIDL 編譯器針對套用 \[ [編碼](/windows/desktop/Midl/encode) \] 或解碼 \[ [](/windows/desktop/Midl/decode) \] 屬性的每個類型，最多會產生三個函數。 例如，針對名為 *MyType* 的使用者定義型別，編譯器會針對 MyType \_ 編碼、MyType 解碼 \_ 和 MyType AlignSize 函數產生程式碼 \_ 。 針對這些函式，編譯器會將原型寫入至 Stub，並將原始程式碼寫入存根 \_ c.c。 一般來說，您可以使用 MyType 解碼，將 *MyType* 物件編碼，並使用 MyType \_ 編碼和解碼緩衝區中的物件 \_ 。 \_如果您需要知道封送處理緩衝區的大小再進行配置，則會使用 MyType AlignSize。

MIDL 編譯器會產生下列編碼函數。 此函式會將 pObject 所指向之物件的資料序列化，並根據控制碼中指定的方法取得緩衝區。 將序列化資料寫入緩衝區之後，您可以控制緩衝區。 請注意，控制碼會繼承先前呼叫的狀態，而緩衝區必須對齊8。

針對隱含控制碼：

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

若為明確的控制碼：

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

下列函式會將來自應用程式儲存體的資料還原序列化為 pObject 所指向的物件。 您可以根據控制碼中指定的方法，提供封送處理的緩衝區。 請注意，這個控制碼可以繼承先前呼叫的狀態，而緩衝區必須對齊8。

針對隱含控制碼：

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

若為明確的控制碼：

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

下列函式會傳回大小（以位元組為單位），其中包含型別實例加上對齊資料所需的任何填補位元組。 這可將相同或不同類型的一組實例序列化為緩衝區，同時確保每個物件的資料都適當對齊。 MyType \_ AlignSize 假設 pObject 所指向的實例將會封送處理到從以8對齊的位移開始的緩衝區。

針對隱含控制碼：

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

若為明確的控制碼：

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

請注意，具有隱含序列化控制碼之隱含系結控制碼和序列化型別的兩個遠端程式都會使用相同的全域控制碼變數。 因此，建議不要將型別序列化和遠端程式混合在具有隱含控制碼的介面中。 如需詳細資訊，請參閱 [隱含與明確的控制碼](implicit-versus-explicit-handles.md)。

 

 