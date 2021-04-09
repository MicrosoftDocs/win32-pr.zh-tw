---
title: 轉譯內容函式
description: 五個 WGL 函數會管理轉譯內容，如下表所述。
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- WGL 函式，呈現內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8d3a8ea0333154d3145711829ab23e262fa485
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933572"
---
# <a name="rendering-context-functions"></a>轉譯內容函式

五個 WGL 函數會管理轉譯內容，如下表所述。



| WGL 函式                                         | Description                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | 建立新的轉譯內容。                                                             |
| [**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | 設定執行緒的目前呈現內容。                                                   |
| [**WglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | 取得執行緒的目前呈現內容控制碼。                                    |
| [**WglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | 取得與執行緒目前呈現內容相關聯之裝置內容的控制碼。 |
| [**WglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | 刪除轉譯內容。                                                                 |



 

[**WglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)函式會採用裝置內容控制碼作為其參數，並傳回轉譯內容控制碼。 所建立的轉譯內容適合在裝置內容控制碼所參考的裝置上進行繪製。 尤其是它的像素格式與裝置內容的像素格式相同。 建立轉譯內容之後，您可以釋放或處置裝置內容。 如需有關建立、取得、釋放和處置裝置內容的詳細資訊，請參閱 [裝置](/windows/desktop/gdi/device-contexts) 內容。

> [!Note]  
> 傳送至 [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) 的裝置內容必須是顯示裝置內容、記憶體裝置內容，或使用每圖元四個或更多位的彩色印表機裝置內容。 裝置內容不能是單色印表機裝置內容。

 

[**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)函式會採用轉譯內容控制碼和裝置內容控制碼作為參數。 執行緒所做的所有後續 OpenGL 呼叫都會透過該轉譯內容進行，並在該裝置內容所參考的裝置上繪製。 建立轉譯內容時，不一定要將裝置內容傳遞至 **wglCreateCoNtext** ，但必須位於相同的裝置上且具有相同的像素格式。 對 **wglMakeCurrent** 的呼叫會在提供的轉譯內容和裝置內容之間建立關聯。 除非您將轉譯內容設為最新狀態，否則無法釋放或處置與目前轉譯內容相關聯的裝置內容。

一旦執行緒有目前的轉譯內容之後，它就可以進行 OpenGL 圖形呼叫。 所有呼叫都必須通過轉譯內容。 如果您從缺少目前呈現內容的執行緒進行 OpenGL 圖形呼叫，就不會發生任何事。

[**WglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)函式不接受任何參數，而且會將控制碼傳回給呼叫執行緒的目前轉譯內容。 如果執行緒沒有目前的轉譯內容，傳回值會是 **Null**。

當您藉由呼叫 [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)來取得與執行緒目前轉譯內容相關聯之裝置內容的控制碼時，會在轉譯內容成為最新的時候建立關聯。

您可以使用兩個控制碼的任一個來呼叫 [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) ，以中斷目前轉譯內容和執行緒之間的關聯：

-   **Null** 轉譯內容控制碼
-   原始呼叫以外的控制碼

使用轉譯內容控制碼參數設定為 **Null** 來呼叫 [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)之後，呼叫的執行緒沒有目前的轉譯內容。 轉譯內容會從其與執行緒的連接釋出，而且轉譯內容與裝置內容的關聯將會結束。 OpenGL 會清除所有繪圖命令，而且可能會釋放一些資源。 在下一次呼叫 **wglMakeCurrent** 之前，不會執行 opengl 繪圖，因為執行緒在重新產生目前的轉譯內容之前，不會呼叫任何 opengl 圖形。

中斷轉譯內容和執行緒之間關聯的第二種方式，是使用不同的轉譯內容來呼叫 **wglMakeCurrent** 。 在這類呼叫之後，呼叫端執行緒會有新的目前轉譯內容，先前的目前轉譯內容會從其連接釋出到執行緒，而先前目前轉譯內容與裝置內容的關聯將會結束。

[**WglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)函式會接受單一參數，也就是要刪除的轉譯內容控制碼。 在呼叫 **wglDeleteCoNtext** 之前，藉由呼叫 [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)讓轉譯內容不是最新，並依適當情況呼叫 [DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) 或 [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) 來刪除或釋放相關聯的裝置內容。

執行緒刪除另一個執行緒目前轉譯內容的轉譯內容時，會發生錯誤。 但是，如果轉譯內容是呼叫執行緒的目前轉譯內容， **wglDeleteCoNtext** 會排清所有 OpenGL 繪圖命令，並在刪除之前將轉譯內容呈現為最新。 在此情況下，依賴 **wglDeleteCoNtext** 讓轉譯內容不是最新的，需要程式設計師刪除或釋放相關聯的裝置內容。

 

 