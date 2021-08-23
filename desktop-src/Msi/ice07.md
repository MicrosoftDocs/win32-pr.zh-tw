---
description: ICE07 會驗證安裝套件是否指定將字型安裝至 FontsFolder。 如果字型安裝在 FontsFolder 以外的資料夾中，安裝程式會建立快捷方式，而不是實際安裝字型。
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a0e555a35c7d5735abe0b14520d000bfeea8c888488ce37b15a78674ff9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581288"
---
# <a name="ice07"></a>ICE07

ICE07 會驗證安裝套件是否指定將字型安裝至 FontsFolder。 如果字型安裝在 FontsFolder 以外的資料夾中，安裝程式會建立快捷方式，而不是實際安裝字型。

ICE07 自訂動作會針對 [字型資料表](font-table.md)中的每個字型執行下列動作。

1.  使用 [字型表格](font-table.md)尋找每個字型標題所屬的字型檔案。
2.  查詢檔案資料表的元件資料 \_ 行，以控制每個檔案的元件。 [](file-table.md)
3.  查詢 \_ [元件資料表](component-table.md) 的目錄資料行，以取得目錄資料表中的索引鍵。
4.  解析 [目錄表](directory-table.md) ，以判斷安裝程式用來安裝字型檔案的資料夾名稱。
5.  如果字型檔案安裝在 FontsFolder 以外的資料夾中，則會張貼錯誤。

## <a name="result"></a>結果

如果 ICE07 發現資料庫指定將字型檔案安裝到 FontsFolder 以外的資料夾中，則會張貼錯誤。

## <a name="example"></a>範例

IC07 會針對所顯示的範例張貼下列錯誤訊息。

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[字型資料表](font-table.md)



| 檔案\_ | FontTitle |
|--------|-----------|
| 默特爾 | Tahoma    |



 

[檔資料表](file-table.md) (部分) 



| 檔案   | 元件\_   |
|--------|---------------|
| 默特爾 | Myrtle \_ 海灘 |



 

[元件資料表](component-table.md) (部分) 



| 元件     | 目錄\_ |
|---------------|-------------|
| Myrtle \_ 海灘 | 沙洲     |



 

在此範例中，會將 Tahoma 的字型對應到字型檔案 Myrtle。 Myrtle 檔案屬於 Myrtle 海灘的元件 \_ 。 目錄資料表的解析會顯示屬於 Myrtle 海灘的所有檔案 \_ 都會安裝在 Sandbar 資料夾中。 因為這不是 FontsFolder，所以 ICE07 會張貼一則錯誤訊息。

請注意，如果 Myrtle 海灘的元件 \_ 確實屬於 Sandbar 資料夾，而不是 FontsFolder，則 Tahoma 的字型可能不屬於 Myrtle \_ 海灘。 可能的錯誤修正方式是在另一個元件中包含 Tahoma，而該元件會安裝在 FontsFolder 目錄中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



