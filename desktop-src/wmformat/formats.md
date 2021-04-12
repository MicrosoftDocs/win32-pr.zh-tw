---
title: 格式
description: 格式
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK，輸入
- Windows Media Format SDK，資料流程
- Windows Media Format SDK，輸出
- Windows Media 格式 SDK，格式
- Advanced Systems Format (ASF) 、輸入
- ASF (Advanced Systems Format) ，輸入
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- Advanced Systems Format (ASF) 、輸出
- ASF (Advanced Systems Format) ，輸出
- Advanced Systems Format (ASF) 、格式
- ASF (Advanced Systems Format) ，格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301623"
---
# <a name="formats"></a>格式

格式的資訊描述特定媒體類型的所有須知事項。 每種格式都有一種主要類型，例如音訊或影片，而且可能有子類型。 格式包含以主要類型為基礎的不同資訊。 音訊和影片格式需要比其他類型更多的資訊。

就像 Windows Media 格式 SDK 的物件會區分輸入數位、串流號碼和輸出編號 (查看輸入 [、串流和](inputs-streams-and-outputs.md) 輸出) ，輸入格式、串流格式和輸出格式之間有很大的差異。 以下說明這些差異：

## <a name="input-formats"></a>輸入格式

輸入格式描述您傳遞至寫入器物件的數位媒體。 如果 ASF 檔案中的串流以編解碼器壓縮，則編解碼器只會支援特定的輸入格式。 當您使用 Windows Media 音訊和影片編解碼器時，可以使用寫入器物件來列舉支援的輸入格式。 寫入檔案時，您必須負責選取符合輸入媒體的輸入格式。

雖然可壓縮資料的編解碼器必須支援輸入媒體格式，但有些輸入格式設定不需要符合資料流程格式。 例如，影片資料流程的輸入格式可能會有不同于資料流程格式所定義的框架大小。 編解碼器會在這些情況下執行轉換。

## <a name="stream-formats"></a>資料流程格式

資料流程格式描述儲存在 ASF 檔案中的媒體格式。 資料流程格式是設定檔中所描述的格式，而且不一定是輸入格式和輸出格式。 如果使用編解碼器壓縮資料流程中的資料，資料流程格式將會與輸入和輸出格式不同。

使用 Windows Media 音訊和影片編解碼器時，您必須從編解碼器取得支援的串流格式清單，以確保您不會嘗試指定程式碼不支援的格式。 您必須在抓取編解碼器格式之後，手動設定某些格式設定，例如影片框架的大小和色彩深度。

## <a name="output-formats"></a>輸出格式

輸出格式描述讀取器 (或同步讀取器) 傳遞至您應用程式的數位媒體。 如果 ASF 檔案中的串流以編解碼器壓縮，則編解碼器只會支援特定的輸出格式。 當您使用 Windows Media 音訊和影片編解碼器時，可以使用 reader 物件來列舉支援的輸出格式。 每個 Windows Media 編解碼器都有預設輸出格式，但您可以選取任何支援的輸出格式來傳遞範例。

雖然壓縮資料的編解碼器必須支援輸出媒體格式，但某些輸出格式設定不需要符合資料流程格式。 例如，影片資料流程的輸出格式可能會有不同于資料流程格式所定義的框架大小。 編解碼器會在這些情況下執行轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](concepts.md)
</dt> </dl>

 

 




