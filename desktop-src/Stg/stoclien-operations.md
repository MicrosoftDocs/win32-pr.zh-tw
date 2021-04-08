---
title: StoClien 作業
description: StoClien 範例會示範用戶端如何使用結構化儲存體。 以下摘要說明 StoClien 作業。
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- StoClien 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682799"
---
# <a name="stoclien-operations"></a>StoClien 作業

[StoClien](structured-storage-client-sample--stoclien-.md)範例會示範用戶端如何使用結構化儲存體。 以下摘要說明 StoClien 作業。

[StoClien](structured-storage-client-sample--stoclien-.md)應用程式視窗用戶端區域是用來顯示以滑鼠或平板電腦裝置所建立的自由格式繪圖。 若要使用滑鼠繪製，請在移動滑鼠時按住滑鼠左鍵。 放開滑鼠左鍵會結束線條的繪製。

以下是作業的摘要，從 Stoclien.exe 的觀點來看，它是 Stoserve.dll COM 伺服器的 COM 用戶端：

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>檔案/開啟
</dt> <dd>

顯示 [開啟] 對話方塊，以取得要開啟之現有檔繪圖檔案的名稱和路徑。 預設值。假設是這些檔案的 PAP 副檔名。 如果在選擇這個功能表項目時對現有的繪圖進行了變更，則會先顯示個別的對話，詢問使用者是否應該將目前的繪圖儲存至其相關聯的複合檔案。

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>檔案/儲存
</dt> <dd>

將目前的繪圖儲存至其相關聯的複合檔案。

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>檔案/另存新檔
</dt> <dd>

顯示 [另存新檔] 對話方塊，以取得要建立之新紙張繪圖檔案的名稱和路徑。 目前的繪圖會成為新檔案的儲存內容，而新的檔案會變成繪圖的新相關複合檔案。

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit
</dt> <dd>

離開 [StoClien](structured-storage-client-sample--stoclien-.md)。

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>繪製/繪圖
</dt> <dd>

開啟 [StoClien](structured-storage-client-sample--stoclien-.md) 用戶端與伺服器中 COPaper 物件之間的繪圖。 此命令會鎖定此用戶端獨佔使用的 COPaper 物件，並防止其他用戶端存取伺服器中的相同 COPaper 實例。

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>繪製/繪製關閉
</dt> <dd>

關閉 [StoClien](structured-storage-client-sample--stoclien-.md) 用戶端與伺服器中 COPaper 物件之間的繪圖。 此命令會解除鎖定此用戶端獨佔使用的 COPaper，並允許其他用戶端存取伺服器中的相同 COPaper 實例。

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>繪製/重繪
</dt> <dd>

在用戶端中重新繪製目前的繪圖資料，此資料保留在伺服器的 COPaper 物件中。

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>繪製/清除
</dt> <dd>

清除目前的繪圖內容，並清除視窗影像。 功能表選取： [畫筆/色彩] 會顯示 [選擇色彩] 對話方塊，以取得用於繪圖的新畫筆色彩。

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>畫筆/中度
</dt> <dd>

選擇繪圖的中寬度。 此功能表選擇上的核取記號表示「中」是目前的畫筆寬度。

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>畫筆/厚
</dt> <dd>

選擇繪圖的寬寬度。 此功能表選擇上的核取記號表示 [寬] 是目前的畫筆寬度。

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>畫筆/細
</dt> <dd>

選擇繪圖的精簡寬度。 此功能表選擇上的核取記號表示瘦是目前的畫筆寬度。

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>接收/連接
</dt> <dd>

將 COPaperSink IPaperSink 介面連接至 COPaper 物件 PaperSink 連接點。 在 [StoClien](structured-storage-client-sample--stoclien-.md) 中重新繪製目前的繪圖影像會依賴接收連接。 此功能表選擇上的核取記號表示已連接重新繪製。

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>接收/中斷連線
</dt> <dd>

中斷 COPaperSink IPaperSink 介面與 COPaper 物件 PaperSink 連接點的連線。 在 [StoClien](structured-storage-client-sample--stoclien-.md) 中重新繪製目前的繪圖影像會依賴接收連接。 此功能表選擇上的核取記號表示重新繪製已中斷連線。

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>說明/StoClien 教學課程
</dt> <dd>

在網頁瀏覽器中開啟 STOCLIEN.HTM 教學課程檔案。

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>說明/StoServe 教學課程
</dt> <dd>

在網頁瀏覽器中開啟 STOSERVE.HTM 教學課程檔案。

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>說明/讀取來源檔案
</dt> <dd>

顯示 [開啟] 對話方塊，讓您可以從這一課或 Windows 記事本中的另一個來源檔案開啟來源檔案。

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>說明/關於 StoClien
</dt> <dd>

顯示此應用程式的 [關於] 對話方塊。

</dd> </dl>

[StoClien](structured-storage-client-sample--stoclien-.md)範例會使用[APPUTIL](./using-visual-studio.md)所提供的許多公用程式類別和服務。 如需 [APPUTIL](./using-visual-studio.md)的詳細資訊，請參閱主要教學課程目錄中的 [APPUTIL](./using-visual-studio.md) 程式庫原始程式碼（位於 [APPUTIL](./using-visual-studio.md) 目錄中）和 Apputil.md。 如需 [APPUTIL](./using-visual-studio.md)的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。

 

 