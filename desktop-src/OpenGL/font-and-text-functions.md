---
title: '字型和文字函數 (OpenGL) '
description: 您可以使用下列函數來管理字型和文字。
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL 函式，文字
- WGL 函式，字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383666"
---
# <a name="font-and-text-functions-opengl"></a>字型和文字函數 (OpenGL) 

您可以使用下列函數來管理字型和文字。



| Windows 函數                                 | Description                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | 建立一組字元點陣圖顯示清單。 字元來自指定之裝置內容的目前字型。 字元會指定為字型字元集內的連續執行。                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | 根據目前選取的裝置內容大綱字型字型，建立一組顯示清單，以與目前的轉譯內容搭配使用。 顯示清單是用來繪製立體字元的 TrueType 字型。 |



 

**WglUseFontBitmaps** 和 **wglUseFontOutlines** 函式會取得裝置內容的控制碼，並使用該裝置內容的目前字型作為點陣圖的來源。 因此，在呼叫 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 之前，必須先設定裝置內容的字型和字型屬性。

[**WglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)和 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)函式也會取得參數，以將字型中的第一個字元轉換成點陣圖顯示清單，以及指定要轉換成顯示清單的字元數的參數。 然後，函數會為指定的連續字元執行建立顯示清單。 例如：

-   若要為所有 Windows 字元集字元建立一組224點陣圖顯示清單，請將這兩個參數分別設定為32和224。
-   若要為所有 OEM 字元集字元建立一組256點陣圖顯示清單，請將這兩個參數分別設定為0和256。
-   若要為任何單一字元集圖像建立單一點陣圖顯示清單，請將這些參數的第二個設為1。

**WglUseFontBitmaps** 和 **wglUseFontOutlines** 函式代表字型中具有空白顯示清單的 null 圖像。

對 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 的呼叫所建立的顯示清單，會連續自動編號。

呼叫 [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) 或 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) 函數之後，請呼叫 [**glCallLists**](glcalllists.md) 來繪製字元字串。 如需範例程式碼，請參閱 [在 Double-Buffered OpenGL 視窗中繪製文字](drawing-text-in-a-double-buffered-opengl-window.md) 。 在此內容中， **glCallLists** 會使用字串中的每個字元做為 **wglUseFontBitmaps** 或 **wglUseFontOutlines** 所建立連續編號顯示清單陣列的索引。

當您完成繪製文字時，請呼叫 [**glDeleteLists**](gldeletelists.md) 函式來釋放 **wglUseFontBitmaps** 和 **wglUseFontOutlines** 所建立的連續一組顯示清單。

 

 




