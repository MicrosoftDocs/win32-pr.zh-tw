---
title: 允許使用者指定裝置和檔案
description: 允許使用者指定裝置和檔案
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog 宏
- MCIWndOpen 宏
- MCIWndOpenInterface 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673523"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="524ce-106">允許使用者指定裝置和檔案</span><span class="sxs-lookup"><span data-stu-id="524ce-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="524ce-107">您可以使用 [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)、 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)、 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏和 [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) 函式，將裝置或檔案與現有的 MCIWnd 視窗建立關聯。</span><span class="sxs-lookup"><span data-stu-id="524ce-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="524ce-108">若要讓應用程式的使用者選取要播放的檔案，請使用 **MCIWndOpenDialog**。</span><span class="sxs-lookup"><span data-stu-id="524ce-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="524ce-109">這個宏會顯示 [ **開啟** ] 對話方塊， (顯示在下列螢幕擷取畫面中) 選擇檔案，並將選取的檔案與目前的 MCIWnd 視窗產生關聯。</span><span class="sxs-lookup"><span data-stu-id="524ce-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![mciwnd 視窗影像](images/mciwnd3.gif)

<span data-ttu-id="524ce-111">您可以讓應用程式的使用者選取要與 MCIWnd 視窗相關聯的檔案，並使用 [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) 和 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)來預覽該檔案。</span><span class="sxs-lookup"><span data-stu-id="524ce-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="524ce-112">**GetOpenFileNamePreview** 函式會顯示 [**開啟**] 對話方塊來選擇檔案，並讓使用者預覽 (播放) 其內容。</span><span class="sxs-lookup"><span data-stu-id="524ce-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="524ce-113">當您在對話方塊中指定現有檔案的名稱時， **GetOpenFileNamePreview** 會提供小型控制項讓使用者預覽檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="524ce-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="524ce-114">您可以使用 **MCIWndOpen**，將指定的檔案（以 **GetOpenFileNamePreview** 或以另一種方式指定）與 MCIWnd 視窗建立關聯。</span><span class="sxs-lookup"><span data-stu-id="524ce-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="524ce-115">您也可以使用 **MCIWndOpen** 來指定要與 MCIWnd 視窗相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="524ce-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="524ce-116">例如，您可以使用裝置名稱，例如 "CDAudio"。</span><span class="sxs-lookup"><span data-stu-id="524ce-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="524ce-117">若要將 MCIWnd 視窗與檔案介面或資料串流介面關聯到多媒體資料，請使用 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏。</span><span class="sxs-lookup"><span data-stu-id="524ce-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="524ce-118">如需檔案和資料流程介面的詳細資訊，請參閱 [AVIFile 函式和宏](avifile-functions-and-macros.md)。</span><span class="sxs-lookup"><span data-stu-id="524ce-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="524ce-119">在建立新檔案或裝置與 MCIWnd 視窗的關聯之前， [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) 和 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) 會關閉目前與該視窗相關聯的任何裝置。</span><span class="sxs-lookup"><span data-stu-id="524ce-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="524ce-120">在使用這些宏之前，您的應用程式不需要關閉任何開啟的裝置。</span><span class="sxs-lookup"><span data-stu-id="524ce-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




