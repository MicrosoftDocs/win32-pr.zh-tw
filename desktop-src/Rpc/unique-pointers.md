---
title: 唯一指標
description: 在 C 程式中，有一個以上的指標可以包含資料的位址。
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adb39d2505daa623f23f47c936fb73d0ecff6e0ad7749c951f9926fd66f33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010988"
---
# <a name="unique-pointers"></a>唯一指標

在 C 程式中，有一個以上的指標可以包含資料的位址。 指標稱為建立資料的 [*別名*](a-glos.md) 。 當指標指向宣告的變數時，也會建立別名。 下列程式碼片段說明這兩種別名方法：


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



在典型的 C 程式中，您可以使用下列定義來指定二進位樹狀結構：


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



有一個以上的指標可以存取樹狀節點的內容。 這通常適用于非分散式應用程式。 不過，這種程式設計樣式會產生更複雜的 RPC 支援程式碼。 用戶端和伺服器 stub 需要額外的程式碼來管理資料和指標。 基礎存根程式碼必須解析位址的各種指標，並判斷哪一個資料複本代表最新版本。

如果您保證指標是應用程式可以存取該記憶體區域的唯一方法，就可以減少處理量。 指標仍可具有 C 指標的許多功能。 例如，它可以在 **null** 和非 **null** 值之間變更或保持不變。 下列範例將說明這點。 指標在呼叫之前為 **null** ，並指向呼叫之後的有效字串：

![在 null 和非 null 值之間變更指標](images/prog-a01.png)

根據預設，MIDL 編譯器會將 \[ [唯一](/windows/desktop/Midl/unique) \] 指標屬性套用至並非參數的所有指標。 您可以使用 \[ [指標 \_ 預設](/windows/desktop/Midl/pointer-default)屬性來變更此預設設定 \] 。

唯一指標具有下列特性：

-   其值可以是 **null**。
-   在呼叫期間，它可以從 **null** 變更為非 **null** 。 當值變更為非 **null** 時，會在傳回時配置新的記憶體。
-   在呼叫期間，它可以從非 **null** 變更為 **null** 。 當值變更為 **Null** 時，應用程式會負責釋放記憶體。
-   值可以從一個非 **null** 值變更為另一個值。
-   唯一指標指向的儲存區無法由作業中的任何其他指標或名稱存取。
-   如果指標沒有 **null** 值，則會將傳回的資料寫入至現有的儲存體。

下列範例示範如何定義唯一指標。

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

在此範例中，參數 *ach* 是傳送至伺服器以使用 RemoteFn 常式處理的字元資料的唯一指標。

 

 