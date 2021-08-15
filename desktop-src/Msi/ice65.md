---
description: ICE65 會檢查環境資料表是否沒有不正確前置詞或附加值。
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 543c75f3abe6cb44a405f41bcb788dc71adf85ae954f013244bfc1cded4e6d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946585"
---
# <a name="ice65"></a>ICE65

ICE65 會檢查 [環境資料表](environment-table.md) 是否沒有不正確前置詞或附加值。

若無法修正 ICE65 回報的警告或錯誤，通常會導致安裝、卸載或修復環境變數時發生問題。 例如，如果該變數的一或多個值具有尾端分隔符號，則只有某些特定變數的值可能會被移除。

## <a name="result"></a>結果

如果環境資料表有不正確前置詞或附加值，ICE65 就會張貼警告或錯誤。

## <a name="example"></a>範例

ICE65 會針對所顯示的範例報告下列錯誤和警告。

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

值結尾的尾端 null (\[ ~ \]) 會將此值標示為任何現有值的前面。 緊接在 null (分號) 的字元會成為此值的分隔符號。 此值也是字串開頭的分號。

若要修正此錯誤，只需刪除前置分號。

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

值中的前置 null (\[ ~ \]) 會將此值標示為附加至任何現有的值。 緊接在 null 之後的字元會變成此值的分隔符號。 在此情況下，該字元是字母 "e"，這也會出現在要附加的字串中間。 此條件 (有一個分隔符號與要附加之字串內的字元相同，) 可能會導致無法預期的結果。

字母 "e" 是通用字母，可能在值中找到。 更好的選擇是 ";" 或一些其他非英數位元。 不過 (不過，如果值是路徑，則 "：" 和 " \\ " 和 "." 是有風險的選擇。 ) 

若要修正此警告，請使用不同的分隔字元。

[環境資料表](environment-table.md)



| 元件 | 目錄 | 屬性         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\];AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ;PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



