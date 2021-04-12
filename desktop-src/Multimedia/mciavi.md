---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- MCI 裝置、MCIAVI 驅動程式
- MCI 命令，MCIAVI 驅動程式
- MCIAVI 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462321"
---
# <a name="mciavi"></a><span data-ttu-id="70e7c-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="70e7c-106">MCIAVI</span></span>

<span data-ttu-id="70e7c-107">AVI 檔案可以包含兩個以上的資料流程，例如影片順序、英文的聲帶和法文的聲帶。</span><span class="sxs-lookup"><span data-stu-id="70e7c-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="70e7c-108">您的應用程式可以使用與檔案中其他資料流程無關的資料流程。</span><span class="sxs-lookup"><span data-stu-id="70e7c-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="70e7c-109">**Digitalvideo** 裝置類型會控制影片檔案。</span><span class="sxs-lookup"><span data-stu-id="70e7c-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="70e7c-110">如需數位視訊裝置可辨識的 MCI 命令清單，請參閱 [數位視訊命令集](digital-video-command-set.md)。</span><span class="sxs-lookup"><span data-stu-id="70e7c-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="70e7c-111">MCIAVI 驅動程式會在 MCI 命令的控制權下播放影片順序和其他資料流程。</span><span class="sxs-lookup"><span data-stu-id="70e7c-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="70e7c-112">資料流程可以包含影像、音訊和調色板。</span><span class="sxs-lookup"><span data-stu-id="70e7c-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="70e7c-113">影像資料可由具有調色板或真色彩資訊的影像所組成。</span><span class="sxs-lookup"><span data-stu-id="70e7c-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="70e7c-114">音訊會在一秒的 thirtieth 內與影片進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="70e7c-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="70e7c-115">但是，如果無法使用音訊硬體，驅動程式只會播放影片串流。</span><span class="sxs-lookup"><span data-stu-id="70e7c-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="70e7c-116">如有必要，MCIAVI 驅動程式可以卸載影片畫面，以播放資料流程，而不會中斷音訊。</span><span class="sxs-lookup"><span data-stu-id="70e7c-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="70e7c-117">您的應用程式可以使用 MCIWnd 視窗類別服務，而不是使用 MCI 命令介面來控制任何 MCI 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="70e7c-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="70e7c-118">此視窗類別會處理管理支援 MCI 裝置之視窗的許多詳細資料，並簡化傳送 MCI 命令所需的程式設計。</span><span class="sxs-lookup"><span data-stu-id="70e7c-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="70e7c-119">您的應用程式可以直接使用 MCIWnd 程式庫服務來控制 MCI 裝置，也可以讓 MCIWnd 顯示工具列、捲軸和功能表，讓使用者控制裝置。</span><span class="sxs-lookup"><span data-stu-id="70e7c-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="70e7c-120">如需 MCIWnd 視窗類別的詳細資訊，請參閱 [MCIWnd 視窗類別](mciwnd-window-class.md)。</span><span class="sxs-lookup"><span data-stu-id="70e7c-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




