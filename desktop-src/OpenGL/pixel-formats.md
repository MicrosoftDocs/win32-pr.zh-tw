---
title: 像素格式
description: 像素格式
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- Windows 上的 OpenGL，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968063"
---
# <a name="pixel-formats"></a>像素格式

*像素格式* 會指定 OpenGL 繪圖介面的數個屬性。 像素格式所指定的部分屬性如下：

-   圖元緩衝區為單一或雙重緩衝。
-   圖元資料是否在 RGBA 或色彩索引表單中。
-   用來儲存色彩資料的位數目。
-   用於深度 (Z 軸) 緩衝區的位數。
-   用於樣板緩衝區的位數目。
-   重迭和基礎平面的數目。
-   各種可見度遮罩。

Microsoft 的適用于 Windows 的 OpenGL 執行會使用 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構來傳達像素格式資料。 結構的成員會指定先前的屬性和其他數個屬性。

給定的裝置內容可以支援數個像素格式。 Windows 會以連續的單一索引值（ (1、2、3、4等等）來識別裝置內容所支援的像素格式，) 。 裝置內容只能有一個目前的像素格式，可從它所支援的像素格式集合中選擇。

在 Windows 中，每個視窗都有它自己目前的像素格式。 例如，這表示應用程式可以同時顯示 RGBA 和色彩索引 OpenGL 視窗，或單一和雙重緩衝的 OpenGL 視窗。 這個每個視窗的像素格式功能僅限於 OpenGL 視窗。

通常，您會取得裝置內容、設定裝置內容的像素格式，然後建立適用于該裝置的 OpenGL 轉譯內容。

> [!Note]  
> 您可以在建立轉譯內容之前設定像素格式，因為轉譯內容會繼承裝置內容的像素格式。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[像素格式函數](pixel-format-functions.md)
</dt> </dl>

 

 




