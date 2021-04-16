---
title: 媒體平臺
description: 媒體基礎和 DirectShow 在 Windows 中提供媒體支援的基礎。
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508095"
---
# <a name="media-platform"></a>媒體平臺

[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 和 [DirectShow](/windows/desktop/DirectShow/directshow) 在 Windows 中提供媒體支援的基礎。 媒體基礎是在 Windows Vista 中引進，作為 DirectShow 的取代。 在 Windows 7 中，已增強媒體基礎，以提供更好的格式支援，包括 *MPEG 4*，以及支援影片捕獲裝置和硬體編解碼器。

## <a name="format-support"></a>格式支援

在 Windows 7 中，[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk)提供廣泛的格式支援，其中包括 *H.264 video、* *MJPEG* 和 *MP3* 的編解碼器;新 *3GP*、 *AAC* 音訊和 *AVI**的來源*;*以及新的檔案* 接收、 *3GP* 和 *MP3*。  ([在媒體基礎中查看支援的媒體格式](../medfound/supported-media-formats-in-media-foundation.md)。 ) 

## <a name="hardware-devices"></a>硬體裝置

[媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 現在支援音訊/影片管線中的下列硬體裝置類型：

-   *UVC 1.1* 影片捕獲裝置，例如網路攝影機
-   音訊捕獲裝置
-   硬體編碼器和解碼器
-   硬體視頻處理器，例如色彩空間轉換器

硬體編解碼器可以執行非常快速的影片轉碼。 例如，假設您想要將 *Windows Media 視訊 (WMV)* 檔傳送到只支援 *3GP* 檔案的行動電話。 使用硬體編碼器時，可以在將檔案傳送到裝置之前，立即轉碼檔案。

硬體裝置會以 proxy 物件 [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 表示，並在管線中使用，就像以軟體為基礎的元件一樣。  (請參閱 [媒體基礎的新功能](../medfound/whats-new-for-media-foundation.md)。 ) 

## <a name="simplified-programming-model"></a>簡化的程式設計模型

在 Windows Vista 中， [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 公開一組相對較低層級的 api。 這些 Api 很有彈性，但可能不適合用來執行工作。 Windows 7 新增了高階 Api，可讓您更輕鬆地以 *c + +* 撰寫媒體應用程式。 這些新的高層級 Api 包括：

-   **MFPlay**。 這些 Api 是針對音訊和影片播放所設計。 它們支援一般的播放作業 (停止、暫停、播放、搜尋、速率控制、音訊音量等等) ，同時隱藏低層級 Api 的詳細資料 (會話和拓撲層) 。
-   **來源讀取器**。 您可以使用這些 Api 從媒體檔案提取未經處理或解碼的資料，而不需要知道任何關於基礎格式的資訊。 例如，您可以從影片檔案取得縮圖點陣圖，或從網路攝影機取得實況影片畫面。
-   **接收寫入器**。 您可以使用這些 Api，藉由傳入未壓縮或編碼的資料來撰寫媒體檔案。 例如，您可以重新編碼或 remix 影片檔案。
-   **轉碼**。 這些 Api 會以最常見的音訊和影片編碼案例為目標。

## <a name="platform-improvements"></a>平臺改善

Windows 7 包含了許多基礎 [媒體基礎](/windows/desktop/medfound/microsoft-media-foundation-sdk) 平臺 api 的增強功能。 Advanced applications 可以直接使用這些 Api;其他應用程式可以間接取得權益。 這些優點包括：

-   影片管線中的增強功能，可減少耗電量和視訊記憶體使用量。
-   新的 *DVXA* 影片處理 api，其使用更具彈性的撰寫模型，且更適合 *HD* 影片格式。
-   改進了外掛程式 (來源和解碼器) 的列舉與管理方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎的新功能](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 