---
description: 本總覽說明 (RIFF) 的資源交換檔案格式，該格式會在 .wav 檔案中使用。 RIFF 是 XAudio2 將載入音訊資料的一般格式。
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: 資源交換檔案格式 (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978182"
---
# <a name="resource-interchange-file-format-riff"></a>資源交換檔案格式 (RIFF)

本總覽說明 (RIFF) 的資源交換檔案格式，該格式會在 .wav 檔案中使用。 RIFF 是 XAudio2 將載入音訊資料的一般格式。

## <a name="riff"></a>RIFF

RIFF 檔案是由多個分隔資料區段（稱為 *區塊*）所組成。

## <a name="fourcc-identifiers"></a>FOURCC 識別碼

區塊中的資料類型是由四個字元的程式碼所表示 (FOURCC) 識別碼。 FOURCC 是在 RIFF 檔案中串連用來識別區塊類型的四個 ASCII 字元所建立的32位不帶正負號的整數。 例如，FOURCC "abcd" 在以位元組由小到大的系統上表示為0x64636261。 FOURCCs 可包含空白字元，因此 "abc" 是有效的 FOURCC。 音訊檔案使用 FOURCC 碼來識別音訊格式區塊、音訊資料區塊，以及音訊格式特定的任何其他區塊。

下表顯示 XAudio2 支援的音訊格式所能預期的 FOURCC 識別碼。 

| 格式 | FOURCC 識別碼                     | 其他資訊                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "RIFF"、"bcp.fmt"、"data"                 |                                                                                                      |
| ADPCM  | "RIFF"、"bcp.fmt"、"data"、"smpl"、"wsmpl" | 如需 ADPCM 特定 FOURCC 識別碼的說明，請參閱 [ADPCM 總覽](adpcm-overview.md) 。 |



 

FOURCC 識別碼 "RIFF"、"bcp.fmt" 和 "data" 通用於所有支援的格式。 下表描述在所有支援的格式中找到的 FOURCC 識別碼。 

| FOURCC 識別碼 | Description                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "RIFF"            | 標準 RIFF 區塊，其中包含的檔案類型值為 "WAVE" 或 "XWMA" （在其資料區段的前四個位元組中）和檔案中的其他區塊（資料區段的其餘部分）。                                   |
| "fmt"             | 包含音訊檔案的格式標頭。 此區塊中的資料會對應到下列其中一個結構： **WAVEFORMATEX**、 **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**。                                                  |
| "data"            | 包含音訊檔案的音訊資料。 在 XAudio2 中，資料區塊的內容將會讀入緩衝區，並傳遞至來源語音作為 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **pAudioData** 成員。 |



 

## <a name="chunks"></a>區塊

RIFF 檔案是由包含零或多個其他區塊的 RIFF 區塊所組成。

-   RIFF 區塊的格式如下：

    "RIFF"，fileSize，資料類型，資料

    其中 "RIFF" 是常值 FOURCC 代碼 "RIFF"， *fileSize* 是4位元組值，可提供檔案中的資料大小，而 *類型類型* 則是可識別特定檔案類型的 FOURCC。 *FileSize* 的值包含資料 *類型* 的大小 FOURCC 加上下列資料的大小，但不包含 "RIFF" FOURCC 或 *fileSize* 大小的大小。 資料包含任何順序的區塊。

-   其他區塊的格式如下：

    ```
    chunkID, chunkSize, data
    ```

    

    其中 *chunkID* 是識別區塊中所含資料的 FOURCC， *chunkSize* 是4位元組值，可提供區塊的資料區段大小，而資料是零或多個位元組的資料。 資料一律會填補到最接近的單字界限。 *chunkSize* 會在區塊中提供有效資料的大小。 它不包含填補、 *chunkID* 大小或 *chunkSize* 大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[使用方法：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[XAudio2 程式設計參考](programming-reference.md)
</dt> </dl>

 

 



