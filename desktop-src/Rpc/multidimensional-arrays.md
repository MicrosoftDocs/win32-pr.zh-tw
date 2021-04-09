---
title: 多維陣列
description: 陣列屬性也可以搭配多維度陣列使用。
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933457"
---
# <a name="multidimensional-arrays"></a>多維陣列

陣列屬性也可以搭配多維度陣列使用。 不過，請小心確保陣列的每個維度都有對應的屬性。 例如：

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

上述陣列是符合標準的陣列 (，其大小為30個元素陣列的大小 d1size )  (具有針對每個) 隨附的 d2len 元素。 Size 的括弧中的逗號 \[ [**\_ 是**](/windows/desktop/Midl/size-is) \] attribute，指定 d1size 中的值會套用至陣列的第一個維度。 同樣地，length 的括弧中的命令 \[ [**\_ 是**](/windows/desktop/Midl/length-is) \] 屬性，表示 d2len 中的值會套用至陣列的第二個維度。

MIDL 2.0 編譯器提供兩種方法來封送處理參數：混合模式 (/**Os**) 和完全解讀的 (/**Oif** 或/**Oicf**) 。 根據預設，MIDL 編譯器會在混合模式中編譯介面。 您不需要明確指定 [**/os**](/windows/desktop/Midl/-os) 參數來取得混合模式封送處理。

完全解讀的方法會完全離線地封送處理資料。 這會大幅減少存根程式碼的大小，但它也會導致效能降低。 在混合模式封送處理中，存根會將某些參數離線封送處理。 雖然這會產生較大的存根大小，但它也可提供更高的效能。

> [!Caution]  
> 在此模式中編譯 IDL 檔案時，請務必小心。 在混合模式中使用多維陣列可能會導致未正確封送處理的參數。 當您的介面定義屬於多維陣列的參數時，建議使用 [**/Oicf**](/windows/desktop/Midl/-oi) 命令列參數。

 

\[[**字串**](/windows/desktop/Midl/string) \] 屬性也可以搭配多維度陣列使用。 屬性會套用至最不重要的維度，例如符合標準的字串陣列。 您也可以使用多維度指標屬性。 例如：

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

在上述範例中，變數 ptr2d 是指標，指向 d1len 大小的指標區塊，其中每個指標都會指向 **long** 的 d2len 指標。

多維陣列與指標陣列不相等。 多維陣列是記憶體中的單一大型資料區塊。 指標的陣列只包含陣列中指標的區塊。 指標指向的資料可以是記憶體中的任何位置。 此外，ANSI C 語法只允許在多維度陣列中未指定最大 (最左邊的) 陣列維度。 因此，下列是有效的語句：

`long a1[] [20]`

將此語句與下列不正確語句進行比較：

`long a1[20] []`

 

 