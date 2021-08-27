---
Description: 以下是視窗類別樣式。
ms.assetid: BE908D51-25DD-45d0-B6AA-28B4C627715B
title: '視窗類別樣式 (Winuser .h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: f7bcca85b3caf5be178facd0ae1804688e8c734ecde40d27d0ffd662a6eb8786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089918"
---
# <a name="window-class-styles"></a>視窗類別樣式

類別樣式定義視窗類別的其他元素。 您可以使用位 OR () 運算子來結合兩個或多個樣式 \| 。 若要將樣式指派給視窗類別，請將樣式指派給 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **樣式** 成員。

## <a name="example"></a>範例

```cpp
    WNDCLASS wc = {};
    wc.lpfnWndProc = s_DropDownWndProc;
    wc.cbWndExtra = sizeof(CTipACDialog *);
    wc.hInstance = g_hInstance;
    wc.hCursor = LoadCursor(NULL, IDC_ARROW);
    wc.hbrBackground = (HBRUSH)(COLOR_WINDOW + 1);
    wc.style = CS_SAVEBITS | CS_DROPSHADOW;
    wc.lpszClassName = s_wzClassName;
    RegisterClass(&wc);
```

GitHub 上[Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/tabletpc/TipAutoComplete/TIPAutoCompleteSDKSample.cpp)的範例。

## <a name="constants"></a>常數


以下是視窗類別樣式。



| 常數/值                                                                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_BYTEALIGNCLIENT"></span><span id="cs_bytealignclient"></span><dl> <dt>**CS \_BYTEALIGNCLIENT**</dt> <dt>0x1000</dt> </dl> | 將位元組界限上視窗的工作區對齊 (x 方向) 。 此樣式會影響視窗的寬度及其在顯示器上的水準位置。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CS_BYTEALIGNWINDOW"></span><span id="cs_bytealignwindow"></span><dl> <dt>**CS \_BYTEALIGNWINDOW**</dt> <dt>0x2000</dt> </dl> | 將位元組界限上的視窗對齊 (x 方向) 。 此樣式會影響視窗的寬度及其在顯示器上的水準位置。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CS_CLASSDC"></span><span id="cs_classdc"></span><dl> <dt>**CS \_CLASSDC**</dt> <dt>0x0040</dt> </dl>                         | 配置一個要由類別中的所有視窗共用的裝置內容。 由於視窗類別是進程特定的，因此應用程式的多個執行緒可能會建立相同類別的視窗。 執行緒也可能會同時嘗試使用裝置內容。 發生這種情況時，系統只允許一個執行緒順利完成其繪製作業。 <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="CS_DBLCLKS"></span><span id="cs_dblclks"></span><dl> <dt>**CS \_DBLCLKS**</dt> <dt>0x0008</dt> </dl>                         | 當使用者按兩下滑鼠，而游標位於屬於類別的視窗內時，會將按兩下訊息傳送至視窗程式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="CS_DROPSHADOW"></span><span id="cs_dropshadow"></span><dl> <dt>**CS \_DROPSHADOW**</dt> <dt>0x00020000</dt> </dl>            | 在視窗上啟用投影效果。 此效果會透過 **SPI \_ SETDROPSHADOW** 開啟和關閉。 一般來說，這會針對小型、短期的視窗（例如功能表）強調其與其他視窗的迭置順序關聯性而啟用。 使用此樣式從類別建立的 Windows 必須是最上層視窗;它們可能不是子視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="CS_GLOBALCLASS"></span><span id="cs_globalclass"></span><dl> <dt>**CS \_GLOBALCLASS**</dt> <dt>0x4000</dt> </dl>             | 表示視窗類別是應用程式全域類別。 如需詳細資訊，請參閱 [關於視窗類別](about-window-classes.md)的「應用程式全域類別」一節。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="CS_HREDRAW"></span><span id="cs_hredraw"></span><dl> <dt>**CS \_HREDRAW**</dt> <dt>0x0002</dt> </dl>                         | 如果移動或大小調整變更工作區的寬度，則會重新繪製整個視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CS_NOCLOSE"></span><span id="cs_noclose"></span><dl> <dt>**CS \_NOCLOSE**</dt> <dt>0x0200</dt> </dl>                         | 停用 [視窗] 功能表上的 [ **關閉** ]。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="CS_OWNDC"></span><span id="cs_owndc"></span><dl> <dt>**CS \_OWNDC**</dt> <dt>0x0020</dt> </dl>                               | 為類別中的每個視窗配置唯一的裝置內容。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CS_PARENTDC"></span><span id="cs_parentdc"></span><dl> <dt>**CS \_PARENTDC**</dt> <dt>0x0080</dt> </dl>                      | 將子視窗的裁剪矩形設定為父視窗的剪切矩形，讓子視窗可以在父系上繪製。 具有 **CS \_ PARENTDC** 樣式位的視窗，會從系統的裝置內容快取接收一般裝置內容。 它不會將父系的裝置內容或裝置內容設定提供給子系。 指定 **CS \_ PARENTDC** 可增強應用程式的效能。 <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CS_SAVEBITS"></span><span id="cs_savebits"></span><dl> <dt>**CS \_SAVEBITS**</dt> <dt>0x0800</dt> </dl>                      | 以點陣圖形式儲存螢幕影像的部分，並以這個類別的視窗遮蔽。 移除視窗時，系統會使用已儲存的點陣圖來還原螢幕影像，包括其他隱藏的視窗。 因此，如果點陣圖使用的記憶體尚未被捨棄，且其他螢幕動作尚未使儲存的影像失效，系統就不會將 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息傳送至隱藏的視窗。 <br/> 這種樣式適用于小型 windows (例如，會短暫顯示的功能表或對話方塊) ，然後在其他螢幕活動發生之前移除。 此樣式會增加顯示視窗所需的時間，因為系統必須先配置記憶體來儲存點陣圖。<br/> |
| <span id="CS_VREDRAW"></span><span id="cs_vredraw"></span><dl> <dt>**CS \_VREDRAW**</dt> <dt>0x0001</dt> </dl>                         | 如果移動或大小調整變更工作區的高度，則會重新繪製整個視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 
