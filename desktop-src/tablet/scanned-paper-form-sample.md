---
description: 在此 C \# 範例中，檔表單已掃描為可移植網狀圖形 (PNG) 檔案，並在執行時間指定為 InkPicture 控制項的背景影像。 此範例會使用訊息方塊來顯示手寫辨識結果。
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: 掃描的紙張表單範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8493384cecdfdbf0186692d52642307f720502f4b953724f444df400cc83c96a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934698"
---
# <a name="scanned-paper-form-sample"></a>掃描的紙張表單範例

在此 C \# 範例中，檔表單已掃描為可移植網狀圖形 (PNG) 檔案，並在執行時間指定為 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的背景影像。 此範例會使用訊息方塊來顯示手寫辨識結果。

此範例包含可延伸標記語言 (XML)  (XML) 檔，Formdata.xml。 XML 檔案包含 PNG 檔案的名稱。 它也包含可 `FieldInfo` 在表單上定義矩形區域的專案，使用者可以在表單上輸入筆跡。 `FieldInfo`下列範例會顯示元素中的資訊：


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



左、上、右和下的元素是每個欄位的圖元座標定義。

此範例會使用 Formdata.xml 中包含的資料來初始化新的 [資料集](/dotnet/api/system.data.dataset?view=netcore-3.1) ：


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



Formdata.xml 中指定的表單影像會以 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的背景載入：


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



然後， [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項會啟用筆墨收集：


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>功能表事件處理常式

應用程式包括在表單頂端顯示之所有功能表的 click 事件處理常式。

### <a name="recognize-menu-item"></a>辨識功能表項目

辨識功能表的 click 事件處理常式會停用控制項的筆墨集合，並檢查手寫辨識器。 如果未安裝辨識器，則會顯示對話方塊。 然後，使用者必須按一下 [筆跡] 或 [畫筆] 功能表選項，以重新啟用筆墨輸入的控制項。

如果已安裝辨識器，則函式會抓取為 `Recognize` 每個表單欄位指定圖元座標的 XML 資料。 座標會轉換成筆墨空間座標，並為每個表單欄位定義一個矩形。 定義矩形之後，此函式會尋找在每個矩形內相交和落在每個矩形內的筆觸。 最後，它會執行筆墨的辨識，並在訊息方塊中顯示結果。

### <a name="ink-menu-item"></a>筆墨功能表項目

筆墨功能表的 click 事件處理常式會啟用 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項。

### <a name="pen-menu-item"></a>畫筆功能表項目

畫筆功能表的 click 事件處理常式會執行下列工作：

-   在變更[system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100))屬性) 之前，停用[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項的筆墨集合 (這是必要的。
-   設定 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 屬性以收集筆跡。
-   重新啟用 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項的筆墨集合，並切換畫筆、選取和橡皮擦功能表以指出現用模式。

### <a name="edit-menu-item"></a>編輯功能表項目

[編輯] 功能表 click 事件處理常式類似于 [畫筆] 功能表事件處理常式。 它會執行下列工作：

-   停用筆墨收集。
-   將 [system.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 屬性設定為 **Select**，讓使用者可以執行筆墨選取。
-   重新啟用筆墨集合，並切換畫筆、編輯和橡皮擦功能表以表示現用模式。

### <a name="eraser-menu-item"></a>橡皮擦功能表項目

橡皮擦功能表的 click 事件處理常式會將 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項 [System.windows.controls.inkcanvas.editingmode](/previous-versions/ms582189(v=vs.100)) 設定為 **Delete**，讓使用者可以清除筆跡。 它也會切換 [畫筆]、[編輯] 和 [橡皮擦] 功能表項目。

### <a name="clear-menu-item"></a>清除功能表項目

清除功能表的 click 事件處理常式會刪除[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項目前的[筆劃](/previous-versions/ms552701(v=vs.100))集合，藉此清除表單上的所有筆墨。

## <a name="closing-the-form"></a>關閉表單

在 Windows 表單設計工具產生的程式碼中，當表單初始化時，會將[InkPicture](/previous-versions/aa514604(v=msdn.10))控制項加入表單的元件清單中。 當表單關閉時，會以表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法處置 InkPicture 控制項，以及表單的其他元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkEdit 控制項](inkedit-control.md)
</dt> <dt>

[InkPicture 控制項](inkpicture-control.md)
</dt> </dl>

 

 
