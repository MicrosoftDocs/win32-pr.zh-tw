---
title: 自動播放
description: 自動播放
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate 宏
- MCIWndPlay 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675583"
---
# <a name="automating-playback"></a><span data-ttu-id="77b43-105">自動播放</span><span class="sxs-lookup"><span data-stu-id="77b43-105">Automating Playback</span></span>

<span data-ttu-id="77b43-106">您可以使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 和 [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 宏，以及 [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) 或 [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) 宏，將應用程式中的播放自動化。</span><span class="sxs-lookup"><span data-stu-id="77b43-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="77b43-107">若要自動播放，請 \_ \_ 在 \**MCIWndCreate \* \* \* dwStyle* 參數中指定 MCIWNDF NOPLAYBAR 和 MCIWNDF NOTIFYMODE 樣式。</span><span class="sxs-lookup"><span data-stu-id="77b43-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="77b43-108">指定 MCIWNDF \_ NOPLAYBAR 樣式來隱藏工具列，以及使用 MCIWNDF \_ NOTIFYMODE 樣式，在裝置停止播放時發出適當的通知訊息。</span><span class="sxs-lookup"><span data-stu-id="77b43-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="77b43-109">您可以使用 **MCIWndPlay** 來播放在 **MCIWndCreate** 中指定的裝置或檔案。</span><span class="sxs-lookup"><span data-stu-id="77b43-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="77b43-110">MCIWndPlay 宏會開始播放其目前播放位置的內容，並繼續結束。</span><span class="sxs-lookup"><span data-stu-id="77b43-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="77b43-111">您可以使用 [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) 或 [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) 宏來摧毀或關閉 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="77b43-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="77b43-112">**MCIWndDestroy** 宏會關閉裝置或檔案，並藉由使其控制碼失效來終結 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="77b43-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="77b43-113">如果您的應用程式可以重複使用 MCIWnd 視窗，請使用 **MCIWndClose** 來關閉裝置，而不會終結視窗。</span><span class="sxs-lookup"><span data-stu-id="77b43-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="77b43-114">您的應用程式可以偵測到裝置何時停止播放，並自動關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="77b43-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="77b43-115">若要這樣做，請 \_ 為 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)的 *dwStyle* 參數指定 MCIWNDF NOTIFYMODE 樣式。</span><span class="sxs-lookup"><span data-stu-id="77b43-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="77b43-116">這會導致裝置在每次變更模式時傳送 [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="77b43-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="77b43-117">您的應用程式可以陷阱此訊息，以判斷裝置是否已停止播放。</span><span class="sxs-lookup"><span data-stu-id="77b43-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="77b43-118">當裝置停止播放時，應用程式會關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="77b43-118">When the device stops playing, the application closes the window.</span></span>

 

 




