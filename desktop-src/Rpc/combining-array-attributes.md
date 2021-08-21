---
title: 合併陣列屬性
description: 只要存根可以使用資訊來判斷陣列的大小以及要傳送到伺服器的位元組數目，就可以在各種組合中提供欄位屬性。
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd440251a658dd5b888df7275f578369419d4b8b2d4f920b263bc5095c4bd948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931751"
---
# <a name="combining-array-attributes"></a>合併陣列屬性

只要存根可以使用資訊來判斷陣列的大小以及要傳送到伺服器的位元組數目，就可以在各種組合中提供欄位屬性。 屬性之間的關聯性是使用下列公式所定義：

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

與屬性相關聯的值必須遵守數個以這些公式為基礎的常見規則。 這三項規則分別是：

-   請勿指定 \[ [**第一個 \_**](/windows/desktop/Midl/first-is) \] 索引值小於零，或 \[ [**\_ 最後**](/windows/desktop/Midl/last-is)一個 \] 值大於 \[ [**max \_**](/windows/desktop/Midl/max-is) \] 。
-   請勿為數組指定負的大小。 定義第一個和最後一個專案，使其產生長度為零或更大的值。 定義 \[ [**最大值 \_ 為**](/windows/desktop/Midl/max-is) \] 零或大於零。 如果使用 [**/error**](/windows/desktop/Midl/-error) 界限檢查選項來叫用 MIDL，則存根會在 \_ 大小小於零時引發例外狀況，或傳送的長度小於零。
-   請勿使用 [ \[ [**長度] \_**](/windows/desktop/Midl/length-is) \] 和 [ \[ [**最後一個] 做 \_ 為**](/windows/desktop/Midl/last-is)屬性，也不會同時有 \] \[ **大小 \_** \] 和 \[ **最後一個 \_** \] 屬性。

因為陣列和指標之間的 C 有接近的關聯性，所以 MIDL 也可讓您使用指標標記法，在參數清單中宣告陣列。 如果參數具有任何通常與陣列相關聯的屬性，MIDL 會將做為型別的指標的參數視為該型別的陣列。

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

在上述範例中，函式 fArray6 和 fArray7 中的陣列和指標參數是相等的。

 

 