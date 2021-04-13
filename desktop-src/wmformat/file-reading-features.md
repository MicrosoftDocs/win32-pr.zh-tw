---
title: 檔案讀取功能
description: 檔案讀取功能
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK，檔案讀取功能
- Windows Media Format SDK，非同步檔案讀取
- Windows Media Format SDK，同步檔案讀取
- Advanced Systems Format (ASF) 、檔案讀取功能
- ASF (Advanced 系統格式) 、檔案讀取功能
- Advanced Systems Format (ASF) 、非同步檔案讀取
- ASF (Advanced 系統格式) 、非同步檔案讀取
- Advanced Systems Format (ASF) ，同步檔案讀取
- ASF (Advanced Systems Format) ，同步檔案讀取
- 非同步檔案讀取
- 同步檔案讀取
- 同步讀取器，檔案讀取功能
- 檔案讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311270"
---
# <a name="file-reading-features"></a>檔案讀取功能

讀取 ASF 檔案是 Windows Media Format SDK 的主要功能之一。 支援兩種類型的讀取：非同步和同步。 非同步檔案讀取是由 reader 物件處理。 同步讀取器物件是用來同步讀取檔案。 如需不同讀取物件的詳細資訊，請參閱 [讀取器物件](reader-object.md) 和 [同步讀取器物件](synchronous-reader-object.md)。

在最基本的非同步檔案讀取案例中，您必須在範例準備就緒時，執行讀取器物件將呼叫的回呼方法。 當您開始讀取檔案之後，您的應用程式會等候範例傳遞給您的回呼方法。 非同步讀取適用于播放程式應用程式，並支援同步讀取時無法使用的功能。 如果您的應用程式需要從網路位置讀取檔案，或與執行 Windows Media Services 的伺服器互動，您必須使用 reader 物件。 讀取器物件的缺點在於每個傳遞的輸出都會使用個別的執行緒。 此外，讀取器物件的彈性，與同步讀取器在如何提供範例之間的彈性。

使用同步讀取器時，您不需要使用任何回呼方法。 相反地，您會選取部分檔案，以使用方法呼叫一次讀取並取出範例。 同步讀取器非常適合內容編輯應用程式的需求，在這種情況下，快速存取特定範例是不可或缺的。 因為同步讀取器不會使用任何回呼方法，所以您可以建立應用程式來讀取具有最少編碼額外負荷的 ASF 檔案。 但是，同步讀取器無法從網路位置開啟檔案，或與執行 Windows Media Services 的伺服器互動，或讀取受 [*DRM*](wmformat-glossary.md)保護的檔案。

下列主題討論讀取器和同步讀取器的功能。



| 主題                                                              | 描述                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [使用者配置的範例支援](user-allocated-sample-support.md) | 討論讀取器和同步讀取器中的緩衝區配置，以及使用者配置可以如何改善效能。 |
| [輸出格式列舉](output-format-enumeration.md)         | 討論輸出格式列舉。                                                                               |



 

此外，[撰寫功能] 區段中的下列主題也適用于檔案讀取：

-   [影片調整大小](video-resizing.md)
-   [色彩空間轉換](color-space-conversion.md)
-   [音訊重新取樣](audio-resampling.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**功能**](features.md)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 




