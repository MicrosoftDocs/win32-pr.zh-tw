---
description: ICE30 會驗證封裝含相同檔案的元件安裝，絕對不會在相同的目錄中多次安裝檔案。
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528658"
---
# <a name="ice30"></a>ICE30

ICE30 會驗證封裝含相同檔案的元件安裝，絕對不會在相同的目錄中多次安裝檔案。

ICE30 會移至 [元件資料表](component-table.md) 中的每個元件，然後從 [目錄資料表](directory-table.md)判斷元件的目標目錄。 然後，它會檢查哪些元件會安裝至相同的目標目錄。 最後，它會使用 [File 資料表](file-table.md) 來確認這些元件中的檔案都沒有相同的名稱。

ICE30 會檢查長檔名 (LFN) 和簡短檔案名 (SFN) 。

ICE30 不會評估目錄解析中的屬性，因為這些屬性會在執行時間變更並改變目錄解析配置。 這表示 ICE30 可以偵測檔案衝突，因為它們的路徑中具有相同屬性的目錄，但未偵測到兩個具有相同值的屬性所產生的衝突。

## <a name="result"></a>結果

ICE30 會針對每一對安裝相同檔案的元件，將錯誤訊息張貼至相同的目錄。

## <a name="example"></a>範例

顯示的範例會傳回下列每個錯誤兩次。



| ICE30 錯誤或警告                                                                                                                                                                                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 錯誤：在 SFN 系統上，有兩個不同的元件在 ' TARGETDIR PRODUCT ' 中安裝了目標檔案 ' README.TXT. 1 ' \\ ： ' Component1 ' 和 ' Component2 '。 這會中斷元件參考計數。                                                                                           | Component1 和 Component2 都有一個名為 ' READEME. 1 ' 的檔案。 使用簡短的檔案名時，安裝程式會將 Dir1 和 Dir2 安裝至相同的目錄 TARGETDIR \\ 產品。<br/> ICE30 會產生兩個錯誤，每個檔案各一個錯誤。 在顯示錯誤位置的撰寫環境中，第一個錯誤是在檔案 [資料表](file-table.md)中的一個檔案專案，第二個是在另一個檔案的位置。<br/> |
| 錯誤：安裝 conditionalized 元件會導致在 LFN 系統上有兩個不同元件的「TARGETDIR 通用工具」中，安裝目標檔案「讀我檔案」 \\ ： ' Component3 ' 和 ' Component4 '。 這會中斷元件參考計數。                      | Component4 在 [元件資料表](component-table.md) 的 [條件] 資料行中有一個專案，而 Component3 則否。 如果 [**VersionNT**](versionnt.md) 為 True，則會安裝 Component4，而且會發生與讀我檔案的衝突。第一次是由 Component3 安裝。<br/> ICE30 會產生4個錯誤，一對 SFN，一個用於 LFN。<br/>                                                                                            |
| 警告：目標檔案 ' README.TXT. 1 ' 可能在 \\ SFN 系統上由兩個不同的 conditionalized 元件安裝在「TARGETDIR 通用工具」中： ' Component4 ' 和 ' Component5 '。 如果條件不是互斥的，這會中斷元件參考計數系統。 | 因為 Component4 和 Component5 在 [元件資料表](component-table.md) 的條件資料行中都有專案，所以可能不會發生此檔案衝突。 ICE30 只會張貼警告，因為條件必須在安裝時決定。<br/> ICE30 會產生4個警告，一對 SFN，一個用於 LFN。<br/>                                                                                            |



 

[元件資料表](component-table.md) (部分) 



| 元件  | 目錄 | 條件 |
|------------|-----------|-----------|
| Component1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[目錄資料表](directory-table.md)



| 目錄 | 上層 \_ 目錄 | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | 產品 \| Component1 產品：。 |
| Dir2      | SOURCEDIR         | 產品：。                     |
| Dir3      | SOURCEDIR         | 常用 \| 工具：         |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ | FileName   |
|-------|-------------|------------|
| File1 | Component1  | README.TXT |
| File2 | Component2  | README.TXT |
| File3 | Component3  | README.TXT |
| File4 | Component4  | README.TXT |
| File5 | Component5  | README.TXT |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




