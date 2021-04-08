---
title: 儲存錄製的內容
description: 儲存錄製的內容
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave 宏
- MCIWndSaveDialog 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673164"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="07fda-105">儲存錄製的內容</span><span class="sxs-lookup"><span data-stu-id="07fda-105">Saving Recorded Content</span></span>

<span data-ttu-id="07fda-106">完成記錄之後，您可以使用 [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) 或 [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) 宏或使用 [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) 函數搭配 **MCIWndSave** 來儲存內容。</span><span class="sxs-lookup"><span data-stu-id="07fda-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="07fda-107">**MCIWndSave** 宏會將資料儲存在與 [MCIWnd] 視窗相關聯的檔案中。</span><span class="sxs-lookup"><span data-stu-id="07fda-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="07fda-108">**MCIWndSaveDialog** 宏可讓使用者指定檔案名，並將記錄的資料儲存在指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="07fda-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="07fda-109">**GetSaveFileNamePreview** 函式會顯示選擇檔案的 [ **SaveAs** ] 對話方塊，讓使用者預覽 (播放) 檔案。</span><span class="sxs-lookup"><span data-stu-id="07fda-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="07fda-110">當現有檔案的名稱指定于 [ **SaveAs** ] 對話方塊時， **GetSaveFileNamePreview** 會在對話方塊中提供一個小控制項，讓使用者預覽檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="07fda-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="07fda-111">您可以使用 **MCIWndSave**，將記錄的資料儲存在使用 **GetSaveFileNamePreview** 所選取的檔案中。</span><span class="sxs-lookup"><span data-stu-id="07fda-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




