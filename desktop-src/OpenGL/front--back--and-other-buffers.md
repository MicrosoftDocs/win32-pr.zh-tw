---
title: 前端、背面和其他緩衝區
description: OpenGL 會在畫面格緩衝區中儲存和操作圖元資料。
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- Windows 上的 OpenGL，緩衝區
- framebuffers OpenGL
- 色彩緩衝區 OpenGL
- 深度緩衝區 OpenGL
- 累積緩衝區 OpenGL
- 樣板緩衝區 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd64f980aad1df8576accd8c37d19521a5368e1fe295393d54c2836f2db8566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082318"
---
# <a name="front-back-and-other-buffers"></a>前端、背面和其他緩衝區

OpenGL 會在畫面格緩衝區中儲存和操作圖元資料。 畫面格緩衝區包含一組邏輯緩衝區：色彩、深度、累積和樣板緩衝區。 色彩緩衝區本身是由一組邏輯緩衝區所組成;此集合可以包含左上角、右上角、左上角、右上角和某些數目的輔助緩衝區。 特定的像素格式或 OpenGL 執行可能無法提供所有的緩衝區。 例如，Microsoft 在 Windows 中的 OpenGL 實作為目前版本不支援 stereoscopic 影像，因此像素格式不能具有左右色彩緩衝區。 此外，目前的版本不支援輔助緩衝區。 如需 OpenGL 緩衝區和在其上操作之 OpenGL 函數的詳細資訊，請參閱 *Opengl 參考手冊* 和 *Opengl 程式設計指南*。

Microsoft 在 Windows 中執行 OpenGL 可支援影像的雙重緩衝。 這是一項技術，可讓應用程式將圖元繪製到螢幕上的緩衝區，然後在該影像可供顯示時，將螢幕緩衝的內容複寫到螢幕上的緩衝區。 雙重緩衝能讓影像變更變得平滑，這對動畫影像來說特別重要。

使用雙重緩衝處理的應用程式可使用兩個色彩緩衝區： front 緩衝區和背景緩衝區。 根據預設，繪製命令會被導向至背景緩衝區)  (的背景緩衝區，而前端緩衝區則會顯示在螢幕上。 當螢幕緩衝區可供顯示時，您可以呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)，Windows 將螢幕緩衝區的內容複寫到螢幕緩衝區。

泛型執行會使用與裝置無關的點陣圖 (DIB) 做為背景緩衝區，而螢幕會顯示為 front 緩衝區。 硬體裝置及其驅動程式可能會使用不同的方法。

雙重緩衝是像素格式的屬性。 若要要求像素格式的雙重緩衝，請 \_ 在呼叫 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)的 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)資料結構中，設定 PFD DOUBLEBUFFER 旗標。

OpenGL core 函數 [**glDrawBuffer**](gldrawbuffer.md)會選取用於寫入和清除的緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[緩衝區函數](buffer-functions.md)
</dt> </dl>

 

 




