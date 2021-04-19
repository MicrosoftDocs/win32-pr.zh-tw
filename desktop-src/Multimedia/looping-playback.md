---
title: 迴圈播放 MCIWnd
description: '迴圈播放 (MCIWnd) '
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106991275"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="e0c95-103">迴圈播放 MCIWnd</span><span class="sxs-lookup"><span data-stu-id="e0c95-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="e0c95-104">MCIWnd 支援以連續迴圈的形式播放。</span><span class="sxs-lookup"><span data-stu-id="e0c95-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="e0c95-105">您可以使用 [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) 宏搭配工具列上的 [ **播放** ] 按鈕，將檔案或裝置的內容重複播放為迴圈。</span><span class="sxs-lookup"><span data-stu-id="e0c95-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="e0c95-106">影片播放裝置 MCIAVI 支援播放迴圈。</span><span class="sxs-lookup"><span data-stu-id="e0c95-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="e0c95-107">若要判斷是否已啟用持續播放，請使用 [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) 宏。</span><span class="sxs-lookup"><span data-stu-id="e0c95-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




