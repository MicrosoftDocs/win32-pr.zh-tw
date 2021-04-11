---
title: 關於圖示
description: 本主題討論圖示。
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- 資源，圖示
- 圖示、作用點
- 圖示，標準
- 標準圖示
- 圖示，自訂
- 自訂圖示
- 圖示，大小
- 建立圖示
- 圖示，顯示
- 圖示，終結
- 圖示，複製
- 圖示，建立
- 顯示圖示
- 終結圖示
- 複製圖示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315004"
---
# <a name="about-icons"></a>關於圖示

系統會在使用者介面中使用圖示來代表物件，例如檔案、資料夾、快捷方式、應用程式和檔。 圖示函式可讓應用程式建立、載入、顯示、排列、建立動畫，以及終結圖示。 如需指定檔案類型圖示的詳細資訊，請參閱 [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)。

本總覽提供下列主題的相關資訊：

-   [圖示作用點](#icon-hot-spot)
-   [圖示類型](#icon-types)
-   [圖示大小](#icon-sizes)
    -   [變更系統小圖示的大小](#to-change-the-size-of-the-system-small-icon)
    -   [取出系統小圖示的大小](#to-retrieve-the-size-of-the-system-small-icon)
    -   [取出系統大型圖示的大小](#to-retrieve-the-size-of-the-system-large-icon)
    -   [取得 shell 小圖示的大小](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [變更大型圖示的大小](#to-change-the-size-of-the-large-icon)
    -   [取得 shell 大型圖示的大小](#to-retrieve-the-size-of-the-shell-large-icon)
-   [圖示建立](#icon-creation)
-   [圖示顯示](#icon-display)
-   [圖示損毀](#icon-destruction)
-   [圖示重複](#icon-duplication)

## <a name="icon-hot-spot"></a>圖示作用點

圖示中的其中一個圖元會指定為 [作用](#icon-hot-spot)點，也就是系統追蹤和辨識為圖示位置的位置。 圖示的作用點通常是位於圖示中間的圖元。 如果您使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式來建立圖示，則可以指定任何圖元作為作用點。

## <a name="icon-types"></a>圖示類型

作業系統提供一組 *標準圖示* ，可供任何應用程式隨時使用。 軟體發展工具組 (SDK) 標頭檔包含標準圖示的識別碼-識別碼開頭為 **IDI \_** 前置詞。

每個標準圖示都有與其相關聯的對應預設影像。 使用者可以隨時取代與任何標準資料指標相關聯的預設影像。

*自訂圖示* 的設計目的是要在特定應用程式中使用，而且可以是任何設計。 以下是數個自訂圖示。

![數個自訂圖示](images/csicn-02.png)

## <a name="icon-sizes"></a>圖示大小

系統使用四個圖示大小：

-   系統小
-   系統大型
-   Shell small
-   Shell 大型

*系統小圖示* 會顯示在視窗標題中。

### <a name="to-change-the-size-of-the-system-small-icon"></a>變更系統小圖示的大小

1.  在主控台中，按一下 [ **顯示**]，然後按一下 [ **外觀** ] 索引標籤。
2.  從 [**專案**] 清單中選取 [**標題] 按鈕**，然後設定 [**大小**] 欄位。

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>取出系統小圖示的大小

-   使用 **sm \_ CXSMICON** 和 **Sm \_ CYSMICON** 來呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)函數。

*系統大型圖示* 主要是由應用程式使用，但它也會顯示在 Alt + Tab 對話方塊中。 [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)、 [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)、 [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)、 [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)、 [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)和 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)函數全都使用系統大型圖示。 系統大型圖示的大小是由 video 驅動程式所定義，因此無法變更。

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>取出系統大型圖示的大小

-   使用 **sm \_ CXICON** 和 **Sm \_ CYICON** 來呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 。

您可以使用 [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)、 [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)、 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)和 [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式來處理系統大型以外大小的圖示。

[ *Shell small] 圖示* 用於 Windows 檔案總管和一般對話方塊中。 目前，這預設為系統小的大小。

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>取得 shell 小圖示的大小

1.  使用 [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式搭配 `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` 來取得系統映射清單的控制碼。
2.  然後呼叫 [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) 函式以取得圖示大小。

桌面上會使用 shell 大型圖示。

### <a name="to-change-the-size-of-the-large-icon"></a>變更大型圖示的大小

1.  在主控台中，按一下 [ **顯示**]，然後按一下 [ **外觀** ] 索引標籤。
2.  從 [**專案**] 清單中選取 [**圖示**]，然後設定 [**大小**] 欄位 (此大小儲存在登錄中，在 [ **HKEY \_ 目前 \_ 使用者主控台] 下，[ \\ 桌面 \\ WindowMetrics \\ Shell 圖示大小**]) 。
3.  按一下 [ **plus** ] 索引標籤，然後選取 [ **使用大圖示** ] 核取方塊。

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>取得 shell 大型圖示的大小

1.  使用 [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式搭配 **SHGFI \_ SHELLICONSIZE** ，以取得系統映射清單的控制碼。
2.  然後呼叫 [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) 函式以取得圖示大小。

根據是否選取 [ **使用大圖示** ] 核取方塊，[開始] 功能表會使用 shell 小型圖示或 shell 大型圖示。

您的應用程式應該提供下列大小的圖示影像群組：

-   48x48，256色彩
-   32x32、16色
-   16x16 圖元、16色

填入要用於註冊視窗類別的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構時，請將 **hIcon** 成員設定為32x32 圖示，並將 **hIconSm** 成員設定為16x16 圖示。 如需類別圖示的詳細資訊，請參閱 [類別圖示](/windows/desktop/winmsg/about-window-classes)。

## <a name="icon-creation"></a>圖示建立

標準圖示是預先定義的，因此不需要建立它們。 若要使用標準圖示，應用程式可以使用 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函式來取得其控制碼。 *圖示控制碼* 是 **HICON** 類型的唯一值，可識別標準或自訂圖示。

若要建立應用程式的自訂圖示，您通常會使用圖形應用程式，並在應用程式的資源定義檔中包含 [圖示資源](./icon-resource.md) 。 在執行時間，您可以呼叫 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 來取得圖示的控制碼。 圖示資源可以包含數個不同顯示裝置的一組影像。 **LoadIcon** 和 **LoadImage** 會自動從目前顯示裝置的群組中選取最適當的圖示。

應用程式也可以使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式在執行時間建立自訂圖示，該函式會根據 [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) 結構的內容建立圖示。 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)函式會以作用點座標和圖示的位元遮罩點陣圖和色彩點陣圖的相關資訊填入結構。

應用程式應該將自訂圖示實作為資源，而且應該使用 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)，而不是在執行時間建立圖示。 使用圖示資源可避免裝置的相依性、簡化當地語系化，以及讓應用程式共用圖示圖形。

[**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)函式可讓應用程式流覽系統的資源，並根據資源資料建立圖示和資料指標。 **CreateIconFromResourceEx** 會根據其他可執行檔或 dll 中的二進位資源資料建立圖示。 應用程式必須在此函式之前，呼叫 [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) 函式和數個資源函數。 **LookupIconIdFromDirectoryEx** 會傳回目前顯示裝置最適當的圖示資料識別碼。

## <a name="icon-display"></a>圖示顯示

您可以使用 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) 函式來抓取圖示的影像，也可以使用 [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) 函數來繪製它。 若要繪製圖示的預設影像，請在 **DrawIconEx** 的呼叫中指定 **DI \_ 相容** 性旗標。 如果您未指定 **DI \_ 相容** 性旗標， **DrawIconEx** 會使用使用者指定的影像繪製圖示。

當系統顯示圖示時，必須從 .exe 或 .dll 檔案解壓縮適當的圖示影像。 系統會使用下列步驟來選取圖示影像：

1.  選取 **RT \_ 群組 \_ 圖示** 資源。 如果有一個以上的這類資源存在，系統會使用資源腳本中所列的第一個資源。
2.  從 **RT \_ 群組 \_ 圖示** 資源選取適當的 **rt \_ 圖示** 影像。 如果有一個以上的映射存在，系統會使用下列準則來選擇映射：
    -   -   選擇最接近所要求大小的影像。
        -   如果有兩個或多個大小的影像，則會選擇符合顯示器色彩深度的影像。
        -   如果沒有任何影像與顯示器的色彩深度完全相符，則會選擇具有最大色彩深度（不超過顯示器的色彩深度）的影像。 如果全部超過色彩深度，則會選擇具有最低色彩深度的色彩深度。

> [!Note]  
> 系統會將8或更多 bpp 的所有色彩深度視為相等。 因此，在相同的資源中，不會有包含 16x16 256 色影像和 16x16 16 色影像的優點，系統只會選擇它所遇到的第一個。 當顯示器處於 8 bpp 模式時，系統會在256色彩的圖示上選擇16色圖示，並使用系統預設調色板來顯示所有圖示。

 

若要顯示動畫圖標，請使用靜態控制項，如下列程式碼片段所示。


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>圖示損毀

當應用程式不再需要使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式所建立的圖示時，它應該會摧毀圖示。 [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)函式會終結圖示控制碼，並釋出圖示所使用的任何記憶體。 應用程式應該只將此函式用於以 **CreateIconIndirect** 建立的圖示;不需要終結其他圖示。

## <a name="icon-duplication"></a>圖示重複

[**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)函式會複製圖示控制碼。 這可讓應用程式或 DLL 取得其他模組所擁有之圖示的控制碼。 然後，如果已釋出其他模組，複製圖示的應用程式仍然可以使用此圖示。

[**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage)函式會根據指定的來源圖示來建立新的圖示。 新圖示可以大於或小於來源圖示。

如需有關在可執行檔 ( .exe) 檔中新增、移除或取代圖示資源的詳細資訊，請參閱 [資源](resources.md)。

[**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)函式會建立圖示的實際複本。

 

 