---
title: 資源檔案格式
description: 本節說明資源編譯器根據資源定義檔的內容所建立的二進位資源檔案格式。
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869789"
---
# <a name="resource-file-formats"></a>資源檔案格式

本節說明資源編譯器根據資源定義檔的內容所建立的二進位資源檔案格式。 這個檔案的副檔名通常是 .res。 連結器會將 .res 檔重新格式化為資源物件檔案，然後將它連結至應用程式的可執行檔。

二進位資源檔是由一些串連的資源專案所組成。 每個專案都包含資源標頭和該資源的資料。 資源標頭在檔案中是以 **DWORD** 對齊，並包含下列各項：

-   包含資源標頭大小的 **DWORD**
-   包含資源資料大小的 **DWORD**
-   資源類型
-   資源名稱
-   其他資源資訊

[**RESOURCEHEADER**](resourceheader.md)結構描述此標頭的格式。 資源的資料會遵循資源標頭，而且是每個資源類型的特定資料。 某些資源也會採用資源專屬的群組標頭結構，以提供一組資源的相關資訊。

## <a name="accelerator-table-resources"></a>快速鍵對應表資源

快速鍵對應表是資源檔中的一個資源專案。 它沒有群組標頭。 [**ACCELTABLEENTRY**](acceltableentry.md)結構描述快速鍵對應表中的每個專案。 允許多個快速鍵對應表。

## <a name="cursor-and-icon-resources"></a>游標和圖示資源

系統會以單一檔案的形式處理每個圖示和資料指標。 不過，這些會儲存在 .res 檔和可執行檔中，做為圖示資源的群組或一組資料指標資源。 圖示和游標資源的檔案格式很類似。 在 .res 檔中，資源群組標頭會遵循所有個別的圖示或資料指標群組元件。

每個圖示元件的格式與 .ico 檔案的格式十分類似。 每個圖示影像都會儲存在 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構中，後面接著色彩與裝置無關的點陣圖 (DIB) 位的圖示 **XOR** 遮罩。 圖示 **和** 遮罩的單色 dib 位遵循色彩 dib 位。

每個資料指標元件的格式類似于當前檔案的格式。 每個資料指標映射都會儲存在 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構中，後面接著游標的 **XOR** 遮罩的單色 dib 位，然後再加上游標 **和** 遮罩的單色 dib 位。 請注意，這兩個資源的點陣圖有差異：與圖示不同的是，游標 XOR 的遮罩不會有色彩 DIB 位。 雖然資料指標遮罩的點陣圖為單色，而且沒有 DIB 標頭或色彩表，但位在對齊和方向方面仍是 DIB 格式。 資料指標和圖示之間有另一個顯著的差異，那就是資料指標沒有熱點和圖示。

圖示和游標資源的群組標頭包含 [**NEWHEADER**](newheader.md) 結構，以及一或多個 [**RESDIR**](resdir.md) 結構。 每個圖示或游標都有一個 **RESDIR** 結構。 群組標頭包含應用程式選取正確的圖示或游標來顯示所需的資訊。 群組標頭和針對群組中的每個圖示或資料指標重複的資料都有固定長度。 這可讓應用程式隨機存取資訊。

## <a name="dialog-box-resources"></a>對話方塊資源

對話方塊也是資源檔中的一個資源專案。 它包含一個 [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) 對話方塊標頭結構，以及對話方塊中每個控制項的一個 [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) 結構。 [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex)和 [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex)結構描述延伸對話方塊資源的格式。

## <a name="font-resources"></a>字型資源

字型會以資源群組的形式儲存在資源檔中。 個別字型組成字型群組。 中的 [字型語句](./font-statement.md) 資源定義語句。RC 檔會定義每個字型。 資源中的每個個別字型都是由相關 fnt 檔案的完整內容所組成。 [**FONTGROUPHDR**](fontgrouphdr.md)結構會遵循 .res 檔案中的所有個別字型元件。

字型資源不會新增至特定應用程式的資源。 相反地，它們通常會新增至副檔名為 fon 的可執行檔。 這些檔案通常是僅限資源的 Dll，而不是應用程式。

## <a name="menu-resources"></a>功能表資源

*功能表資源* 是由 [**MENUHEADER**](menuheader.md)結構，後面接著一或多個 [**NORMALMENUITEM**](normalmenuitem.md)或 [**POPUPMENUITEM**](popupmenuitem.md)結構所組成，每個功能表項目的功能表範本都有一個。 [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md)和 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md)結構描述擴充功能表資源的格式。

## <a name="message-table-resources"></a>訊息資料表資源

*訊息資料表* 是包含格式化文字的資源，可顯示為錯誤訊息或訊息方塊。 訊息資料表資源中的主要結構是 [**訊息 \_ 資源 \_ 資料**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) 結構。

## <a name="version-resources"></a>版本資源

版本資源中的主要結構是 [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) 結構。 其他結構包含儲存語言資訊資料的 [**VarFileInfo**](varfileinfo.md) 結構，以及使用者定義字串資訊的 [**StringFileInfo**](stringfileinfo.md) 。 版本資源中的所有字串都採用 Unicode 格式。 每個資訊區塊都在 **DWORD** 界限上對齊。

 

 