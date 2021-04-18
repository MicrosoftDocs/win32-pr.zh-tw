---
description: ICE64 會檢查使用者設定檔中的新目錄在漫遊案例中是否已正確移除。
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513717"
---
# <a name="ice64"></a>ICE64

ICE64 會檢查使用者設定檔中的新目錄在漫遊案例中是否已正確移除。

若無法修正 ICE64 回報的警告或錯誤，通常會導致在卸載期間完全清除電腦時發生問題。 當已安裝應用程式的漫遊使用者第一次登入電腦時，會將所有配置檔案複製到電腦上。 在漫遊設定檔下載) 之後的公告 (，安裝程式會確認目錄是否已存在，因此不會在卸載時將它刪除。 這會將目錄永久保留在使用者的電腦上。

## <a name="result"></a>結果

如果未移除使用者設定檔中應移除的新目錄，ICE64 會在漫遊情況下張貼警告或錯誤。

## <a name="example"></a>範例

ICE64 會針對所顯示的範例報告下列錯誤。

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

資料夾 ' MyOtherFolder ' 是自訂的設定檔資料夾。 因為它未列在 RemoveFile 資料表中，所以在某些情況下不會移除它。

若要修正這個錯誤，請在 RemoveFile 資料表中建立資料夾的資料列。

[目錄資料表](directory-table.md)



| 目錄     | 目錄 \_ 父系 | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| MyFolder      | AppDataFolder     | DataFolder  |
| MyOtherFolder | AppDataFolder     | DataFolder2 |



 

[RemoveFile 資料表](removefile-table.md)



| FileKey | 元件\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Key1    | Component1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



