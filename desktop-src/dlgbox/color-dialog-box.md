---
title: 色彩對話方塊
description: 顯示模式對話方塊，讓使用者可以選擇特定的色彩值。
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- '[色彩] 對話方塊'
- 部分色彩對話方塊
- '[完整色彩] 對話方塊'
- 自訂色彩對話方塊
- RGB 色彩模型
- HSL 色彩模型
- '色調飽和度亮度 (HSL) '
- 'HSL (色調飽和度亮度) '
- 'RGB (red 綠 blue) '
- '紅色綠色藍色 (RGB) '
- '[勾點]，[色彩] 對話方塊'
- 預先定義的對話方塊
- 對話方塊、色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bdfb1543de80ac105d4a6012a0c95ff46cd8da1fef204ed573d14d05a6dfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726388"
---
# <a name="color-dialog-box"></a>色彩對話方塊

顯示模式對話方塊，讓使用者可以選擇特定的色彩值。 使用者可以從一組基本或自訂調色盤中選擇色彩。 或者，使用者也可以藉由修改對話方塊使用者介面的 RGB 或色調、飽和度、亮度 (HSL) 色彩值來產生色彩值。 [ **色彩** ] 對話方塊會傳回使用者所選取之色彩的 RGB 值。

您可以藉由初始化 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構並將結構傳遞至 [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))函式，來建立和顯示 [**色彩**] 對話方塊。 藉由為 **CHOOSECOLOR** 結構設定不同的參數值，您可以影響 [色彩] 對話方塊的顯示方式。 例如，您可以顯示對話方塊的完整或部分使用者介面版本。 下圖顯示 [ **色彩** ] 對話方塊的完整使用者介面版本。

![色彩對話方塊](images/colordialogboxxp.png)

如果使用者按一下 [ **確定]** 按鈕， [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 會傳回 **TRUE**。 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的 **rgbResult** 成員包含使用者所選取之色彩的 RGB 色彩值。 RGB 色彩值會指定組成所選色彩之個別紅色、綠色和藍色色彩的濃度。 個別的值範圍從0到255。 使用 [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue)、 [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)和 [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) 宏從 RGB 色彩值解壓縮個別色彩。

如果使用者取消 [ **色彩** ] 對話方塊或發生錯誤， [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) 會傳回 **FALSE** ，且不會定義 **rgbResult** 成員。 若要判斷錯誤的原因，請呼叫 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值。

本節涵蓋下列主題

-   [完整和部分色彩對話方塊](#full-and-partial-color-dialog-boxes)
-   [自訂色彩對話方塊](#customizing-the-color-dialog-box)
    -   [提供 [色彩] 對話方塊的自訂範本](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [若要啟用 [色彩] 對話方塊的勾點程式](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [色彩對話方塊所使用的色彩模型](#color-models-used-by-the-color-dialog-box)
    -   [RGB 色彩模型](#rgb-color-model)
    -   [HSL 色彩模型](#hsl-color-model)
    -   [將 HSL 值轉換為 RGB 值](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>完整和部分色彩對話方塊

[色彩] 對話方塊具有完整的版本和部分的使用者介面版本。 完整版本包含基本控制項，而且具有可讓使用者建立自訂色彩的其他控制項。 部分版本具有可顯示基本和自訂色彩調色板的控制項，使用者可以從中選取色彩值。

[色彩] 對話方塊的部分版本包含 [ **定義自訂色彩** ] 按鈕。 使用者可以按一下此按鈕以顯示完整的版本。 您可以藉由在 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的 **旗標** 成員中設定 **CC \_ FULLOPEN** 旗標，指示 [色彩] 對話方塊一律顯示完整版本。 若要防止使用者建立自訂色彩，您可以設定 **CC \_ PREVENTFULLOPEN** 旗標來停用 [ **定義自訂色彩** ] 按鈕。

基本色彩代表指定裝置上可用的色彩選項。 實際顯示的色彩數目是由顯示驅動程式所決定。 例如，VGA 驅動程式會顯示48色彩，而單色顯示驅動程式只會顯示16。

自訂色彩是您指定或使用者建立的色彩。 當您建立 [色彩] 對話方塊時，您必須使用 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的 **lpCustColors** 成員來指定16個自訂色彩的初始值。 如果已開啟 [色彩] 對話方塊的完整版本，則使用者可以使用下列其中一種方法來建立自訂色彩：

-   將游標移至色譜控制項和亮度投影片控制項
-   在 **紅色**、 **綠色** 和 **藍色** 編輯控制項中輸入 RGB 值
-   在 **色調**、 **飽和度** 和 **亮度** 編輯控制項中輸入 HSL 值

若要將新的自訂色彩加入自訂色彩顯示，使用者可以按一下 [ **加入自訂色彩** ] 按鈕。 這也會讓對話方塊將新色彩的 RGB 值複製到 **lpCustColors** 成員所指向陣列中的對應元素。 若要在呼叫 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))之間保留新的自訂色彩，您應該為數組配置靜態記憶體。 如需 RGB 和 HSL 色彩模型的詳細資訊，請參閱 [[色彩] 對話方塊所使用的色彩模型](#color-models-used-by-the-color-dialog-box)。

## <a name="customizing-the-color-dialog-box"></a>自訂色彩對話方塊

若要自訂 [色彩] 對話方塊，您可以使用下列任何一種方法：

-   當您建立對話方塊時，在 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構中指定值
-   提供自訂範本
-   提供勾點程式

您可以在 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的 **旗標** 成員中設定旗標，以修改 [色彩] 對話方塊的外觀和行為。 例如，您可以設定 **CC \_ SOLIDCOLOR** 旗標，指示對話方塊只顯示純色。 若要讓對話方塊一開始選取黑色以外的色彩，請設定 **CC \_ RGBINIT** 旗標，並在 **rgbResult** 成員中指定色彩。

您可以提供 [色彩] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。 [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))函式會使用您的自訂範本來取代預設範本。

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>提供 [色彩] 對話方塊的自訂範本

1.  藉由修改在 $. d 檔案中指定的預設範本來建立自訂範本。 在 [預設色彩] 對話方塊範本中使用的控制項識別碼是在 [中] 檔案中定義。
2.  使用 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構來啟用範本，如下所示：
    -   如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **CC \_ ENABLETEMPLATE** 旗標。 使用結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。

        -或者-

    -   如果您的自訂範本已在記憶體中，請設定 **CC \_ ENABLETEMPLATEHANDLE** 旗標。 您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。

您可以針對 [色彩] 對話方塊提供 [**CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) 的勾點程式。 攔截程式可以處理傳送至對話方塊的訊息。 它也可以使用已註冊的訊息來控制對話方塊的行為。 如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>若要啟用 [色彩] 對話方塊的勾點程式

1.  在 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的 **旗標** 成員中設定 **CC \_ ENABLEHOOK** 旗標。
2.  在 **lpfnHook** 成員中指定攔截程式的位址。

處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。 此訊息的 *lParam* 參數是用來初始化對話方塊之 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構的指標。

當使用者按一下 [**確定]** 按鈕時，對話方塊會將已註冊的 [**COLOROKSTRING**](colorokstring.md)訊息傳送到攔截程式。 攔截程式可拒絕選取的色彩，並在收到此訊息時，強制對話方塊維持開啟狀態。 攔截程式可以將 [**SETRGBSTRING**](setrgbstring.md) 註冊的訊息傳送至對話方塊，強制對話方塊選取特定的色彩。 若要使用這些已註冊的訊息，您必須將 **COLOROKSTRING** 和 **SETRGBSTRING** 常數傳遞給 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式，以取得訊息識別碼。 然後，您可以使用識別碼來偵測和處理從對話方塊傳送的訊息，或將訊息傳送至對話方塊。

## <a name="color-models-used-by-the-color-dialog-box"></a>色彩對話方塊所使用的色彩模型

[色彩] 對話方塊的自訂色彩延伸，可讓使用者使用 RGB 或 HSL 值來指定色彩。 不過， [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) 結構只使用 RGB 值來報告使用者所建立或選取的色彩。

-   [RGB 色彩模型](#rgb-color-model)
-   [HSL 色彩模型](#hsl-color-model)
-   [將 HSL 值轉換為 RGB 值](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>RGB 色彩模型

RGB 模型是用來指定顯示器的色彩，以及發出燈光的其他裝置。 有效的紅色、綠色及藍色值的範圍是從0到255，0表示最小強度和255，表示最大濃度。 下圖顯示如何結合紅色、綠色和藍色的主要色彩，以產生四個額外的色彩。 針對顯示裝置 (，當紅色、綠色和藍色值設定為0時，會顯示黑色色彩結果。 在顯示技術中，黑色是所有色彩都沒有。 ) 

![重迭的紅色、綠色和藍色圓形](images/rgbcolormodel.png)

下表列出 RGB 模型的八種色彩及其相關聯的 RGB 值。



| Color   | RGB 值    |
|---------|---------------|
| 紅色     | 255、0、0     |
| 綠色   | 0、255、0     |
| 藍色    | 0、0、255     |
| 11：青色    | 0、255、255   |
| 桃紅色 | 255、0、255   |
| 黃色  | 255、255、0   |
| 白色   | 255、255、255 |
| 黑色   | 0, 0, 0       |



 

系統會以32位 RGB 值儲存內部色彩，其十六進位形式如下：0x00bbggrr。

低序位位元組包含相對強度的紅色值;第二個位元組包含綠色的值;第三個位元組包含藍色的值。 高序位位元組必須為零。

您可以使用 [**rgb**](/windows/desktop/api/wingdi/nf-wingdi-rgb) 宏來取得以紅色、綠色和藍色元件的指定濃度為基礎的 rgb 值。 使用 [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue)、 [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)和 [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) 宏從 RGB 色彩值解壓縮個別色彩。

### <a name="hsl-color-model"></a>HSL 色彩模型

[色彩] 對話方塊會提供用來指定 HSL 值的控制項。 下圖顯示色彩範圍控制項，以及顯示在 [色彩] 對話方塊中的亮度投影片控制項。 此圖也會顯示使用者可使用這些控制項指定的值範圍。

![色譜和亮度比例](images/colordialogranges.png)

在 [色彩] 對話方塊中，[飽和度] 和 [亮度] 值的範圍必須介於0到240之間，而色相值必須在0到239的範圍內。

### <a name="converting-hsl-values-to-rgb-values"></a>將 HSL 值轉換為 RGB 值

在 [色彩] 對話方塊的 [Comdlg32.dll 中提供的對話方塊套裝程式含程式碼，可將 HSL 值轉換成對應的 RGB 值。 下表列出 RGB 模型的八種色彩，以及其相關聯的 HSL 和 RGB 值。



| Color   | HSL 值      | RGB 值      |
|---------|-----------------|-----------------|
| 紅色     |  (0、240、120)    | (255, 0, 0)     |
| 黃色  |  (40、240、120)   |  (255、255、0)    |
| 綠色   |  (80、240、120)   |  (0、255、0)      |
| 11：青色    |  (120、240、120)  |  (0、255、255)    |
| 藍色    |  (160、240、120)  |  (0、0、255)      |
| 桃紅色 |  (200、240、120)  |  (255、0、255)    |
| 白色   |  (0、0、240)      |  (255、255、255)  |
| 黑色   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
