---
description: PSI 剖析器篩選範例
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: PSI 剖析器篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104571397"
---
# <a name="psi-parser-filter-sample"></a>PSI 剖析器篩選範例

## <a name="description"></a>Description

PSI 剖析器篩選器會接收從 MPEG-2 傳輸串流 (PSI) 的程式特定資訊，並從程式關聯資料表中解壓縮程式資訊 (PAT) 和程式對應表 (PMT) 。 此資訊可讓應用程式設定 MPEG-2 信號信號。 篩選準則支援自訂介面 [**IMpeg2PsiParser**](impeg2psiparser.md)，可用於抓取 PSI 資訊。

此篩選器是針對 MPEG-2 裝置所設計，例如 IEEE 1394 MPEG 攝影機和 D VHS 裝置。 如需詳細資訊，請參閱 [MSTape 驅動程式](mstape-driver.md) 。 數位電視廣播來源應該使用 .TIF 篩選器來取得程式資訊。

## <a name="usage"></a>使用方式

您可以在 GraphEdit 中測試 PSI 剖析器篩選器，如下所示：

1.  啟動 GraphEdit。
2.  插入 MPEG 2 傳輸來源。 MPEG-2 攝影機和 D VHS 裝置在影片捕獲來源類別中會顯示為「Microsoft AV/C 磁帶次級裝置」。
3.  將來源篩選連接至 MPEG-2 信號篩選器。
4.  使用 demux 上的屬性頁面，建立具有 "MPEG-2 PSI" 媒體類型的輸出圖釘。 此 pin 會提供 PAT 和 PMT 區段。
5.  使用 [demux] 屬性頁可將 PID 0x00 對應到輸出圖釘。 將內容類型設定為 [MPEG2 PSI 區段]。
6.  將 demux 輸出圖釘連接到 PSI 剖析器，如下圖所示。

    ![psi 剖析器篩選圖形](images/psi-parser.png)

7.  執行圖形，以便將 PSI 資料摘要至 PSI 剖析器篩選器。 當篩選器對 PAT 區段進行解碼時，它會自動將 PMT Pid 對應到 demux 上的相同輸出釘選，以便接收到 PMT 區段。
8.  使用 [PSI 剖析器] 屬性頁選取程式編號。 [屬性] 頁面中的 [基本資料流程] 清單會顯示與所選程式中的每個基本資料流程相關聯的 PID 和資料流程類型。 屬性頁的設計目的是要辨識 ISO/IEC 13818-1 中定義的資料流程類型。
9.  在 [ **音訊 pid** ] 編輯方塊中輸入音訊 pid 號碼，並在 [ **影片 pid** ] 編輯方塊中輸入影片 pid 號碼。
10. 按一下 [ **視圖程式** ] 按鈕。 PSI 剖析器會在 demux 上設定輸出針腳，以符合程式串流資訊和轉譯釘選。

> [!Note]  
> 您可以利用 [PSI 剖析器] 屬性頁讓測試變得更容易，並提供可設定 MPEG-2 信號的範例程式碼。 不建議應用程式使用。 應用程式應該以程式設計的方式設定 demux。

 

若要在應用程式中使用 PSI 剖析器篩選器，請先從 MPEG-2 來源建立篩選圖形至 MPEG-2 demux。 此步驟的程式碼不會顯示在此處，因為確切的圖表設定將取決於來源。

接下來，在 demux 上建立 PSI 資料的輸出圖釘。 將 PID 0x00 （保留給 PAT 區段）對應至此 pin，如下列程式碼所示：


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



如需詳細資訊，請參閱 [使用 Mpeg-2 信號](using-the-mpeg-2-demultiplexer.md)。

將 PSI 剖析器篩選器新增至圖形，並將它連接到 demux 上的輸出圖釘。 查詢 [**IMpeg2PsiParser**](impeg2psiparser.md) 介面的 PSI 剖析器。 現在，執行圖形並等候 EC \_ 程式 \_ 變更事件，以表示新的 PAT 或 PMT 區段。 此事件是由 PSI 剖析器篩選準則所定義的自訂事件。 當您收到 EC \_ 程式 \_ 已變更事件時，您可以藉由呼叫 **IMpeg2PsiParser** 方法來取得可用的 PSI 資訊。 本節將說明您最常需要的方法。

若要取得程式的數目，請使用 [**IMpeg2PsiParser：： GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) 方法：


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



若要取得特定程式的程式編號，請使用 [**IMpeg2PsiParser：： GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) 方法：


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



程式編號可用來取得個別程式的 PMT 專案。 若要取得程式中的基本資料流程數目，請使用 [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) 方法：


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



針對每個基本資料流程， [**IMpeg2PsiParser：： GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) 方法會傳回 PID，而 [**IMpeg2PsiParser：： GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) 方法會傳回資料流程類型：


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



PID 和 stream 型別可讓您設定新的輸出針腳（以 MPEG-2 信號的輸出）。 這可能需要對原始來源有所瞭解。 例如，ISO/IEC 13818-1 會將0x80 到0xFF 的資料流程類型定義為「使用者私用」，但以 MPEG-2 為基礎的其他標準可能會將其他意義指派給這些類型。

當圖形正在執行時，MPEG-2 信號信號可以建立新的 pin 和新的 PID 對應，但您必須停止圖形來連接釘選。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ PSIParser。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 範例](directshow-samples.md)
</dt> <dt>

[**IMpeg2PsiParser 介面**](impeg2psiparser.md)
</dt> </dl>

 

 
