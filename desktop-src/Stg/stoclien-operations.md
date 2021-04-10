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
# <a name="stoclien-operations"></a><span data-ttu-id="35c23-105">StoClien 作業</span><span class="sxs-lookup"><span data-stu-id="35c23-105">StoClien Operations</span></span>

<span data-ttu-id="35c23-106">[StoClien](structured-storage-client-sample--stoclien-.md)範例會示範用戶端如何使用結構化儲存體。</span><span class="sxs-lookup"><span data-stu-id="35c23-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="35c23-107">以下摘要說明 StoClien 作業。</span><span class="sxs-lookup"><span data-stu-id="35c23-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="35c23-108">[StoClien](structured-storage-client-sample--stoclien-.md)應用程式視窗用戶端區域是用來顯示以滑鼠或平板電腦裝置所建立的自由格式繪圖。</span><span class="sxs-lookup"><span data-stu-id="35c23-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="35c23-109">若要使用滑鼠繪製，請在移動滑鼠時按住滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="35c23-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="35c23-110">放開滑鼠左鍵會結束線條的繪製。</span><span class="sxs-lookup"><span data-stu-id="35c23-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="35c23-111">以下是作業的摘要，從 Stoclien.exe 的觀點來看，它是 Stoserve.dll COM 伺服器的 COM 用戶端：</span><span class="sxs-lookup"><span data-stu-id="35c23-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="35c23-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>檔案/開啟</span><span class="sxs-lookup"><span data-stu-id="35c23-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="35c23-113">顯示 [開啟] 對話方塊，以取得要開啟之現有檔繪圖檔案的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="35c23-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="35c23-114">預設值。假設是這些檔案的 PAP 副檔名。</span><span class="sxs-lookup"><span data-stu-id="35c23-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="35c23-115">如果在選擇這個功能表項目時對現有的繪圖進行了變更，則會先顯示個別的對話，詢問使用者是否應該將目前的繪圖儲存至其相關聯的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>檔案/儲存</span><span class="sxs-lookup"><span data-stu-id="35c23-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="35c23-117">將目前的繪圖儲存至其相關聯的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>檔案/另存新檔</span><span class="sxs-lookup"><span data-stu-id="35c23-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="35c23-119">顯示 [另存新檔] 對話方塊，以取得要建立之新紙張繪圖檔案的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="35c23-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="35c23-120">目前的繪圖會成為新檔案的儲存內容，而新的檔案會變成繪圖的新相關複合檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span><span class="sxs-lookup"><span data-stu-id="35c23-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="35c23-122">離開 [StoClien](structured-storage-client-sample--stoclien-.md)。</span><span class="sxs-lookup"><span data-stu-id="35c23-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c23-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>繪製/繪圖</span><span class="sxs-lookup"><span data-stu-id="35c23-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="35c23-124">開啟 [StoClien](structured-storage-client-sample--stoclien-.md) 用戶端與伺服器中 COPaper 物件之間的繪圖。</span><span class="sxs-lookup"><span data-stu-id="35c23-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="35c23-125">此命令會鎖定此用戶端獨佔使用的 COPaper 物件，並防止其他用戶端存取伺服器中的相同 COPaper 實例。</span><span class="sxs-lookup"><span data-stu-id="35c23-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>繪製/繪製關閉</span><span class="sxs-lookup"><span data-stu-id="35c23-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="35c23-127">關閉 [StoClien](structured-storage-client-sample--stoclien-.md) 用戶端與伺服器中 COPaper 物件之間的繪圖。</span><span class="sxs-lookup"><span data-stu-id="35c23-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="35c23-128">此命令會解除鎖定此用戶端獨佔使用的 COPaper，並允許其他用戶端存取伺服器中的相同 COPaper 實例。</span><span class="sxs-lookup"><span data-stu-id="35c23-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>繪製/重繪</span><span class="sxs-lookup"><span data-stu-id="35c23-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="35c23-130">在用戶端中重新繪製目前的繪圖資料，此資料保留在伺服器的 COPaper 物件中。</span><span class="sxs-lookup"><span data-stu-id="35c23-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>繪製/清除</span><span class="sxs-lookup"><span data-stu-id="35c23-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="35c23-132">清除目前的繪圖內容，並清除視窗影像。</span><span class="sxs-lookup"><span data-stu-id="35c23-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="35c23-133">功能表選取： [畫筆/色彩] 會顯示 [選擇色彩] 對話方塊，以取得用於繪圖的新畫筆色彩。</span><span class="sxs-lookup"><span data-stu-id="35c23-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>畫筆/中度</span><span class="sxs-lookup"><span data-stu-id="35c23-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="35c23-135">選擇繪圖的中寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="35c23-136">此功能表選擇上的核取記號表示「中」是目前的畫筆寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>畫筆/厚</span><span class="sxs-lookup"><span data-stu-id="35c23-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="35c23-138">選擇繪圖的寬寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="35c23-139">此功能表選擇上的核取記號表示 [寬] 是目前的畫筆寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>畫筆/細</span><span class="sxs-lookup"><span data-stu-id="35c23-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="35c23-141">選擇繪圖的精簡寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="35c23-142">此功能表選擇上的核取記號表示瘦是目前的畫筆寬度。</span><span class="sxs-lookup"><span data-stu-id="35c23-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>接收/連接</span><span class="sxs-lookup"><span data-stu-id="35c23-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="35c23-144">將 COPaperSink IPaperSink 介面連接至 COPaper 物件 PaperSink 連接點。</span><span class="sxs-lookup"><span data-stu-id="35c23-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="35c23-145">在 [StoClien](structured-storage-client-sample--stoclien-.md) 中重新繪製目前的繪圖影像會依賴接收連接。</span><span class="sxs-lookup"><span data-stu-id="35c23-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="35c23-146">此功能表選擇上的核取記號表示已連接重新繪製。</span><span class="sxs-lookup"><span data-stu-id="35c23-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>接收/中斷連線</span><span class="sxs-lookup"><span data-stu-id="35c23-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="35c23-148">中斷 COPaperSink IPaperSink 介面與 COPaper 物件 PaperSink 連接點的連線。</span><span class="sxs-lookup"><span data-stu-id="35c23-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="35c23-149">在 [StoClien](structured-storage-client-sample--stoclien-.md) 中重新繪製目前的繪圖影像會依賴接收連接。</span><span class="sxs-lookup"><span data-stu-id="35c23-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="35c23-150">此功能表選擇上的核取記號表示重新繪製已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="35c23-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>說明/StoClien 教學課程</span><span class="sxs-lookup"><span data-stu-id="35c23-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="35c23-152">在網頁瀏覽器中開啟 STOCLIEN.HTM 教學課程檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>說明/StoServe 教學課程</span><span class="sxs-lookup"><span data-stu-id="35c23-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="35c23-154">在網頁瀏覽器中開啟 STOSERVE.HTM 教學課程檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>說明/讀取來源檔案</span><span class="sxs-lookup"><span data-stu-id="35c23-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="35c23-156">顯示 [開啟] 對話方塊，讓您可以從這一課或 Windows 記事本中的另一個來源檔案開啟來源檔案。</span><span class="sxs-lookup"><span data-stu-id="35c23-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="35c23-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>說明/關於 StoClien</span><span class="sxs-lookup"><span data-stu-id="35c23-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="35c23-158">顯示此應用程式的 [關於] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="35c23-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="35c23-159">[StoClien](structured-storage-client-sample--stoclien-.md)範例會使用[APPUTIL](./using-visual-studio.md)所提供的許多公用程式類別和服務。</span><span class="sxs-lookup"><span data-stu-id="35c23-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="35c23-160">如需 [APPUTIL](./using-visual-studio.md)的詳細資訊，請參閱主要教學課程目錄中的 [APPUTIL](./using-visual-studio.md) 程式庫原始程式碼（位於 [APPUTIL](./using-visual-studio.md) 目錄中）和 Apputil.md。</span><span class="sxs-lookup"><span data-stu-id="35c23-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="35c23-161">如需 [APPUTIL](./using-visual-studio.md)的詳細資訊，請參閱 [如何建立範例](how-to-build-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="35c23-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 