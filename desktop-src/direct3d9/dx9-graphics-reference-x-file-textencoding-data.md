---
description: 資料物件包含實際資料或該資料的參考。 每個資料物件都有一個指定資料類型的對應範本。 下列各節將討論資料物件的表單和部分。
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: '資料 (X 檔案格式，文字編碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385744"
---
# <a name="data-x-file-format-text-encoding"></a>資料 (X 檔案格式，文字編碼) 

資料物件包含實際資料或該資料的參考。 每個資料物件都有一個指定資料類型的對應範本。 下列各節將討論資料物件的表單和部分。

## <a name="form-identifier-and-name"></a>表單、識別碼和名稱

資料物件具有下列格式。


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



識別碼是強制性的，且必須符合先前定義的資料類型或基本類型。 不過，名稱是選擇性的。

## <a name="data-members"></a>資料成員

資料成員可以是下列其中一項：資料物件、資料參考、整數清單、浮動清單或字串清單。

資料物件是嵌套的資料物件。 這可表示檔案格式的階層式本質。 階層中允許的嵌套資料物件類型可能會受到限制。

資料參考是先前遇到之資料物件的參考，如下列範例所示。


```
{
  name |
  UUID |
  name UUID
}
```



整數清單是以分號分隔的整數清單，如下列範例所示。


```
1; 2; 3;
```



Float 清單是以分號分隔的浮動清單，如下列範例所示。


```
1.0; 2.0; 3.0;
```



字串清單是以分號分隔的字串清單，如下列範例所示。


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字編碼方式](text-encoding.md)
</dt> </dl>

 

 



