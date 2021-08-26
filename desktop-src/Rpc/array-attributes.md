---
title: 陣列屬性
description: C 語言中的陣列和指標之間有接近的關聯性。
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba7bdaa08352a96987066313d4db074872f28b71ec0be0856a32522a849029c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073518"
---
# <a name="array-attributes"></a>陣列屬性

C 語言中的陣列和指標之間有接近的關聯性。 以參數形式傳遞至函式時，會將陣列名稱稱視為陣列第一個元素的指標，如下列範例所示：


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



在本機呼叫中，您可以使用指標參數來建立3到記憶體的內容，並檢查其他位址的內容：


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



當用戶端將指標傳遞至遠端程式時，用戶端存根會將指標和其指向的資料都傳送出去。 除非指標受限於其對應的資料，否則所有用戶端的記憶體都必須在每次遠端呼叫時傳輸。 藉由在介面定義中強制強型別，MIDL 會將用戶端存根處理限制為對應至指定之指標的資料。

陣列的大小和傳送至遠端電腦的陣列元素範圍可以是常數或變數。 當這些值是變數，因此在執行時間決定時，您必須使用 IDL 檔案中的屬性來指定要傳輸的陣列元素數目。 下列 MIDL 屬性支援陣列界限。



| 屬性                             | 描述                                             | 預設 |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[**第一個 \_ 是**](/windows/desktop/Midl/first-is)\]   | 已傳送之第一個陣列元素的索引。           | 0       |
| \[[ **last \_**](/windows/desktop/Midl/last-is)\]     | 最後傳送的陣列元素索引。            | \-      |
| \[[**長度 \_ 為**](/windows/desktop/Midl/length-is)\] | 已傳送的陣列元素總數。             | \-      |
| \[[**最大值 \_ 為**](/windows/desktop/Midl/max-is)\]       | 最大有效陣列索引值。                        | \-      |
| \[[**最小值 \_ 為**](/windows/desktop/Midl/min-is)\]       | 最低有效陣列索引值。                         | 0       |
| \[[**大小 \_ 為**](/windows/desktop/Midl/size-is)\]     | 配置給陣列的陣列元素總數。 | \-      |



 

> [!Note]  
> **最小值 \_ 是** 不會在 RPC 中執行的屬性。 最小陣列索引一律會被視為零。

 

 

 