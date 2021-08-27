---
description: MFTrace 是一種工具，可為 Microsoft 媒體基礎應用程式產生追蹤記錄。
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: 使用 MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469965"
---
# <a name="using-mftrace"></a>使用 MFTrace

MFTrace 是一種工具，可為 Microsoft 媒體基礎應用程式產生追蹤記錄。

MFTrace 會使用繞道程式庫連結至媒體基礎 API 呼叫並產生追蹤記錄。 MFTrace 也可以從使用事件追蹤 Windows (ETW) 或軟體追蹤預處理器 (WPP) 的任何元件記錄追蹤，以產生追蹤。 您可以從 MFTrace 啟動新的進程，或將 MFTrace 附加至現有的進程，以產生追蹤記錄。

## <a name="usage"></a>使用方式

**mftrace** \[**-** *進程* \] \[ **-c** *ConfigurationFile* \] \[ **-dc**- \] \[ **es** \] \[ **-k** *關鍵字* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-** ？ \] \[{*命令* \|*ETL_FILE*}\]




| 命令列引數 | Description | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong><em>處理序識別碼或進程名稱</em><br /> | 附加至正在執行的進程。<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong><em>設定檔</em><br /> | 從指定的設定檔讀取設定。 請參閱 <a href="mftrace-configuration-file.md">MFTrace 設定檔</a>。<br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br /> | 停用子進程的追蹤。 依預設，子進程會啟用追蹤。<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | 啟用公用符號。<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong><em>關鍵字</em><br /> | 關鍵字的逗號分隔清單。 請參閱 <a href="mftrace-keywords.md">MFTrace 關鍵字</a>。<br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong><em>層級</em><br /> | 追蹤層級。<br /><ul><li>0：無</li><li>1：重大</li><li>2：錯誤</li><li>3：警告</li><li>4：資訊</li><li>5：詳細資訊</li><li>16： Debug</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong><em>輸出</em>檔<br /> | 將追蹤輸出寫入至指定的檔案。 根據預設，輸出會移至 <strong>stdout</strong>。<br /> 如果指定了輸出檔，則副檔名必須是下列其中一項：<br /><ul><li>etl：事件追蹤記錄 (ETL) 檔。</li><li>.log 或 .txt：文字檔。</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | 啟用詳細資訊模式。<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | 顯示使用資訊。<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>命令</em><br /> | 用來建立新進程的命令列引數。<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | 現有 ETL 檔案的名稱。 如果有提供此引數，ETL 檔案就會轉換成文字輸出。<br /> | 




 

## <a name="environment-variables"></a>環境變數

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

若要追蹤使用 Windows 軟體追蹤預處理器 (WPP) 的元件，請將此環境變數設定為 [指定追蹤訊息格式的路徑] (TMF 元件的) 檔。

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

如果已啟用 (**es**) 的符號查閱，請設定此環境變數以指定符號路徑。

</dd> </dl>

## <a name="examples"></a>範例

建立新的進程並追蹤該處理常式：

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

將 MFTrace 附加至現有的進程：

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

將追蹤輸出傳送至文字檔：

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

追蹤 ETW 或 WPP 事件：

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> 第一個範例會產生文字檔。 第二個範例會產生 ETL 檔案。

 

將 ETL 檔案轉換成文字檔：

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>備註

根據預設，MFTrace 只會產生繞道追蹤。 若要產生 ETW 或 WPP 追蹤，您必須提供設定檔。 設定檔會提供追蹤提供者的名稱。 如需詳細資訊，請參閱 [MFTrace 設定檔](mftrace-configuration-file.md)。

MFTrace 可將輸出傳送至下列目的地：

-   **stdout** (預設) 。
-   文字檔。
-   二進位 ETL 檔案。

如果您要記錄 ETW/WPP 追蹤，ETL 檔案是最有效率的選項，因為追蹤資料會儲存為二進位 blob。 追蹤會話完成後，您可以使用 MFTrace 將 ETL 檔案轉換成文字檔。

> [!Note]  
> 針對繞道追蹤，文字輸出的效率與 ETL 檔案一樣有效率。 因此，如果您只記錄繞道追蹤 (沒有 ETW/WPP 追蹤) ，則建議使用文字輸出。

 

針對繞道追蹤，您必須將 MFTrace 附加到執行中的進程 (**-a**) 或使用 MFTrace 來建立新的進程。 針對 ETW/WPP 追蹤，MFTrace 會接聽設定檔中所列的任何事件提供者。

您可以透過 **-k** 命令列選項，或在設定檔中指定追蹤關鍵字，以篩選追蹤結果。 不過，較常見的用法是記錄所有追蹤，然後使用腳本或 **grep** 來搜尋特定的字串模式。

## <a name="interpreting-the-trace-results"></a>解讀追蹤結果

您可以使用 MFTrace 來回答有關媒體基礎應用程式或元件內發生的問題。 下表列出一些一般問題。 第二個數據行提供可協助回答問題的搜尋字串。




| 問題 | 搜尋字串 | 
|----------|----------------|
| 是否發生錯誤？ | "0xc00d" | 
| 拓撲是否正確解析？ | "CTopologyHelpers：： Trace" | 
| 媒體會話是否已啟動？ | "MESessionStarted" | 
| 播放了哪些檔案？ | "CMFSourceResolverDetours" | 
| 來源串流的媒體類型有哪些？ | "New stream"、"MENewStream"、"CMFMediaSourceDetours：： TracePD" | 
| 來來源資料流是否會產生範例？ | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| 播放是否達到資料的結尾？ | "MEEndOfStream", "MEEndOfPresentation" | 
| 格式是否變更？ | 「MEStreamFormatChanged」 (媒體來源) 、「新格式」、「MESessionStreamSinkFormatChanged」 (媒體接收器)  | 
| 建立了哪些物件？ | "COle32ExportDetours：： CoCreateInstance" | 
| 媒體基礎是否轉換管線中的 (MFTs) 處理任何資料？ | "CMFTransformDetours：:P rocessOutput"，"CMFTransformDetours：:P rocessInput" | 
| MFTs 上設定了哪些狀態？ | "CMFTransformDetours：:P rocessMessage" | 
| MFT 要求輸入資料嗎？ | "MF_E_TRANSFORM_NEED_MORE_INPUT" (同步的 MFT) ，"METransformNeedInput" (非同步 MFT) 。 | 
| 非同步 MFT 是否會產生輸出資料？ | 「ProcessOutputs 可用」 | 
| 媒體接收要求範例嗎？ | "MEStreamSinkRequestSample" | 
| 媒體接收是否收到範例？ | "CMFStreamSinkDetours：:P rocessSample" | 
| DirectShow：已處理的範例為何？ | "sample"、"CMemInputPinDetours" | 
| DirectShow：使用了哪一個篩選圖形？ | "CGraphHelpers：： Trace" | 
| 是否有多個進程？ | CreateProcess<blockquote>[!Note]<br />也請尋找處理序識別碼，此識別碼會出現在每個追蹤行的開頭。</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 




