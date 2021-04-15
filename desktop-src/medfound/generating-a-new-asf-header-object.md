---
description: 產生新的 ASF 標頭物件
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: 產生新的 ASF 標頭物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510789"
---
# <a name="generating-a-new-asf-header-object"></a>產生新的 ASF 標頭物件

若要將 ContentInfo 物件中包含的資訊轉換成二進位 ASF 標頭物件格式，應用程式必須呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)。 此呼叫必須在產生資料封包，且 ContentInfo 物件包含更新資訊之後進行。 **GenerateHeader** 會傳回媒體緩衝區的指標，其中包含有效格式的標頭資訊。 然後，應用程式可以在新的 ASF 檔案開頭，寫入媒體緩衝區所指向的資料。

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>使用 ContentInfo 物件撰寫新的標頭物件

1.  呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。
2.  呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) ，將設定檔物件提供給 ContentInfo 物件。 如需建立設定檔的詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。
3.  呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) ，並在 *pIHeader* 參數中傳遞 **Null** ，並在 *pcbHeader* 參數中接收已填入 ContentInfo 物件的大小。 應用程式可以使用此值來配置記憶體，或將包含標頭物件的媒體緩衝區。

    收到的標頭大小包含填補大小，這會根據標頭物件的實際大小來調整。 標頭物件的大小上限為 10 MB。 如果大小超過此值， **GenerateHeader** 就會失敗，並出現 MF \_ E \_ ASF \_ INVALIDDATA 錯誤。

4.  呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ，在步驟3中建立所接收大小的媒體緩衝區。
5.  再次呼叫 **GenerateHeader** ，以從步驟4所建立之媒體緩衝區中的 ContentInfo 物件產生新的 ASF 標頭物件。

    媒體緩衝區中的資料長度會更新，並在 *pcbHeader* 參數中傳回新的大小。

6.  在檔案的開頭寫入媒體緩衝區的內容。 應用程式可以使用位元組資料流程來執行寫入作業。 如需範例程式碼，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。

### <a name="example"></a>範例

下列範例程式碼示範如何建立 ContentInfo 物件，並產生媒體緩衝區來儲存新的標頭物件。 如需使用此程式碼的完整範例，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[為新檔案撰寫 ASF 標頭物件](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



