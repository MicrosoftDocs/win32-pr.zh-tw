---
title: 影片調整大小
description: 影片調整大小
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK，調整大小的影片
- Windows Media Format SDK，調整大小影片
- Advanced Systems Format (ASF) 、影片大小調整
- ASF (Advanced Systems Format) 、影片大小調整
- Advanced Systems Format (ASF) ，調整大小影片
- ASF (Advanced Systems Format) ，調整大小影片
- 影片調整大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183283"
---
# <a name="video-resizing"></a>影片調整大小

當您定義影片資料流程的設定時，您必須指定影片框架的寬度和高度。 此影片大小會決定在檔案的 [資料] 區段中編碼的影片框架大小。 不過，設定檔中的影片大小不會決定或限制您傳遞給寫入器的輸入媒體大小，或是您從讀取器收到的輸出媒體大小。 寫入器可以調整影片畫面的大小，以符合您應用程式的需求。

影片影像大小可視為三個階段：輸入影片大小、串流影片大小和輸出影片大小。

輸入影片大小是您以範例形式傳遞至寫入器物件的框架大小。 您可以將此大小定義為其中一個必要的影片輸入屬性。 如需輸入屬性的詳細資訊，請參閱 [列舉輸入格式](to-enumerate-input-formats.md)。

串流影片大小是 ASF 檔案的 [資料] 區段中的框架大小。 您可以將此大小定義為設定檔中的其中一個必要的串流設定。 如果您要寫入檔案，且輸入影片大小與串流影片大小不同，則寫入器會在編碼時調整框架大小。 如需影片串流屬性的詳細資訊，請參閱設定 [影片串流](configuring-video-streams.md)。

輸出影片大小是由讀取器或同步讀取器所提供的框架大小。 您可以將此大小定義為其中一個必要的影片輸出屬性。 如果您要讀取檔案，而且輸出影片大小與串流影片大小不同，則讀取器會在解碼時調整畫面的大小。

您無法將 stream 影片大小設定為奇數圖元寬的數位。 如果您將影片資料流程的寬度設定為奇數值，寫入器將不會接受該設定檔，否則產生的影片將會以一側的黑色線條向下編碼來構成差異。

調整影片大小時，請務必小心。 影像通常會以原始解析度查看其最佳效果。 調整影像大小通常會造成失真，並讓文字難以辨識。 如果您要將影片壓縮成低位速率，您也會發現調整大小扭曲可能會導致嚴重的壓縮成品。

Windows Media 視訊9螢幕編解碼器不支援調整大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案寫入功能**](file-writing-features.md)
</dt> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> <dt>

[**使用輸出**](working-with-outputs.md)
</dt> </dl>

 

 




