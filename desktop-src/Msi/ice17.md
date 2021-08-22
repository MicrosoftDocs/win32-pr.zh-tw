---
description: ICE17 會檢查本主題結尾範例中所顯示的狀況。
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e9714edebd666173a82c75fc6e8fed54a511c64adaa387013648b2f190e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529198"
---
# <a name="ice17"></a>ICE17

ICE17 會檢查本主題結尾範例中所顯示的狀況。

## <a name="result"></a>結果

ICE17 會顯示範例中每一種情況的錯誤或警告訊息。 下表顯示這類訊息的範例。



| ICE17 錯誤或警告                                                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 按鈕：對話方塊的 Button1： MyDialog 沒有在 ControlEvent 資料表中定義的事件。 錯誤 <br/>                                                                                                                | [ControlEvent 資料表](controlevent-table.md)中沒有列出一個[按鈕控制項](pushbutton-control.md)。 如果 ICE17 在 [控制項資料表](control-table.md)的 [屬性] 資料行中未設定 [**啟用控制項**] 屬性或 [**可見控制項**] 屬性的按鈕上傳回這個錯誤，請檢查控制項是否也在 [ControlCondition 資料表](controlcondition-table.md)中有專案。 如果 [條件] 資料行中的值變更為 [True]、[啟用] 或 [顯示]，則此控制項可能會意外地啟用或顯示。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap： Control 的 Bitmap1： Bitmap1 of Dialog： MyDialog 不在二進位資料表中。 錯誤 <br/>                                                                                                                              | 有 [點陣圖控制項](bitmap-control.md) 或 [圖示控制項](icon-control.md)，但對應的點陣圖或圖示未列在 [二進位資料表](binary-table.md)中。 將點陣圖或圖示加入至二進位資料表。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup： Control 的 RadioButton1： RadioButton1 of Dialog： MyDialog 不在選項按鈕資料表中。 警告 <br/>                                                                                                   | 在 [屬性] 資料行中具有值的 [RadioButtonGroup 控制項](radiobuttongroup-control.md) ，以及 [控制資料表](control-table.md)的 [屬性] 資料行。在 [屬性] 資料行中未設定 [間接](indirect-control-attribute.md) 位。 ICE17 會張貼警告，因為安裝程式使用屬性的值做為選項按鈕資料表的外鍵，但該資料表的主鍵遺漏了值。 如果設定了 [間接](indirect-control-attribute.md) 位，則不會將控制項所列出的屬性當做屬性使用，相反地，它是用來做為實際使用之屬性的名稱。<br/> 如果在執行時間建立控制項，則可以忽略這個警告。 例如，如果在安裝期間有使用中的檔案，則 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)上的[ListBox 控制項](listbox-control.md)只會在執行時間建立。<br/> |
| ListBox：控制項的最 MyDialog：對話方塊的 ListBox1：不在 ListBox 資料表中。 警告 <br/>                                                                                                                        | 在[控制資料表](control-table.md)的 [屬性] 資料行中有一個值的[ListBox 控制項](listbox-control.md)，在 [屬性] 資料行中未設定[間接](indirect-control-attribute.md)位。 ICE17 會張貼警告，因為安裝程式使用屬性的值做為 [ListBox 資料表](listbox-table.md)的外鍵，但該資料表的主鍵遺漏了值。 如果設定了 [間接](indirect-control-attribute.md) 位，控制項會變更屬性的值，該屬性的名稱是與此控制項相關聯之屬性的值。<br/> 如果在執行時間建立控制項，則可以忽略這個警告。 例如，如果在安裝期間有使用中的檔案，則 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)上的[ListBox 控制項](listbox-control.md)只會在執行時間建立。<br/>                                |
| ComboBox：控制項的 ComboBox1：對話方塊的 ComboBox1： ByDialog 不在 ComboBox 資料表中警告 <br/>                                                                                                                     | 在[控制資料表](control-table.md)的 [屬性] 資料行中有一個值，而在 [屬性] 資料行中沒有設定[間接](indirect-control-attribute.md)位的[ComboBox 控制項](combobox-control.md)。 ICE17 會張貼警告，因為安裝程式使用屬性的值做為 [ComboBox 資料表](combobox-table.md)的外鍵，但該資料表的主鍵遺漏了值。 如果設定了 [間接](indirect-control-attribute.md) 位，控制項會變更屬性的值，該屬性的名稱是與此控制項相關聯之屬性的值。<br/> 如果在執行時間建立控制項，則可以忽略這個警告。 例如，如果在安裝期間有使用中的檔案，則 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)上的[ListBox 控制項](listbox-control.md)只會在執行時間建立。<br/>                            |
| ListView：控制項的 ListView1：對話方塊的 ListView1： MyDialog 不在 ListView 資料表中。 警告 <br/>                                                                                                                    | 在[控制資料表](control-table.md)的 [屬性] 資料行中有一個值，而在 [屬性] 資料行中沒有設定[間接](indirect-control-attribute.md)位的[ListView 控制項](listview-control.md)。 ICE17 會張貼警告，因為安裝程式使用屬性的值做為 [ListView 資料表](listview-table.md)的外鍵，但該資料表的主鍵遺漏了值。 如果設定了 [間接](indirect-control-attribute.md) 位，控制項會變更屬性的值，該屬性的名稱是與此控制項相關聯之屬性的值。<br/> 如果在執行時間建立控制項，則可以忽略這個警告。 例如，如果在安裝期間有使用中的檔案，則 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)上的[ListBox 控制項](listbox-control.md)只會在執行時間建立。<br/>                            |
| 點陣圖： ' Bitmap2 ' 用於控制項： ' Button2 ' 的對話方塊： ' MyDialog ' 在二進位資料表中找不到錯誤 <br/>                                                                                                                         | 有一個 [按鈕](pushbutton-control.md) 控制項或 [核取方塊控制項](checkbox-control.md) ， [控制資料表](control-table.md) 的文字資料行在包含點陣圖或圖示的 [二進位資料表](binary-table.md) 記錄中不包含外鍵。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 點陣圖： ' Bitmap3 ' 用於控制項： ' RadioButton2 ' 的對話方塊：在二進位資料表中找不到 ' MyDialog '，或<br/> 圖示： ' Icon1 ' 用於控制項： ' RadioButton3 ' 的對話方塊： ' MyDialog ' 在二進位資料表中找不到<br/> 錯誤 <br/> | 有一個 [RadioButtonGroup 控制項](radiobuttongroup-control.md) ， [選項按鈕資料表](radiobutton-table.md) 的文字資料行沒有包含點陣圖或圖示之 [二進位資料表](binary-table.md) 記錄的外鍵。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 圖片控制項：對話方塊的 ' Button3 '： ' MyDialog ' 同時有 Icon 和 Bitmap 屬性設定錯誤 <br/>                                                                                                                     | 在[控制資料表](control-table.md)的 [屬性] 資料行中設定的[圖示](icon-control-attribute.md)位或[點陣圖](bitmap-control-attribute.md)位，都有一個 [[按鈕](pushbutton-control.md)]、[[核取方塊]](checkbox-control.md)或 [ [RadioButtonGroup](radiobuttongroup-control.md) ] 控制項。 您無法同時設定這兩個屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>範例

[控制資料表](control-table.md) (部分) 



| 對話\_ | 控制      | 類型             | 屬性 | 屬性     | Text       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | 按鈕       | 0          |              | 確定         |
| MyDialog | Bitmap1      | 點陣圖           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | 按鈕       | 262144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262144     |              | Property2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524288     |              | Property3  |
| MyDialog | Button3      | 按鈕       | 786432     |              | Ambiguous1 |



 

[選項按鈕資料表](radiobutton-table.md) (部分) 



| 屬性\_ | 單 | Text    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

下列資料表是空的：

-   [ControlEvent 資料表](controlevent-table.md)
-   [ListBox 資料表](listbox-table.md)
-   [ComboBox 資料表](combobox-table.md)
-   [ListView 資料表](listview-table.md)
-   [二進位資料表](binary-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




