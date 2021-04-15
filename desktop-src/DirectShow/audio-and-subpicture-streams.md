---
description: 音訊和子圖片串流
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: 音訊和子圖片串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467895"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="f1f2e-103">音訊和子圖片串流</span><span class="sxs-lookup"><span data-stu-id="f1f2e-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="f1f2e-104">DVD-Video 光碟最多可有八個音訊串流（編號為0到7），每個串流都有最多六個不同的通道。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="f1f2e-105"> (請注意，音訊和子圖片串流的編號是從零開始，而標題、角度和家長能從1開始編號。 ) 在任何指定時間都只能選取其中一個串流。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="f1f2e-106">針對 subpictures，最多可使用32串流，但在任何特定時間都只能啟用一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="f1f2e-107">光碟通常是以預設的音訊和子圖片串流來撰寫，但應用程式可以讓使用者查看所有可用資料流程的清單，然後選取所需語言的清單。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="f1f2e-108">此程式中的基本步驟在音訊和子圖片串流中都相同。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="f1f2e-109">決定可供標題使用的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="f1f2e-110">逐一查看串流，並取得每個資料流程的資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="f1f2e-111">從傳回的地區設定識別碼中取出語言代碼 (LCID) 並建立人們可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="f1f2e-112">填入清單方塊或其他使用者介面 (UI) 控制項，讓使用者選取慣用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="f1f2e-113">在 DVD 範例應用程式中，對話方塊中的 CAudioLangDlg：： MakeAudioStreamList 方法會示範基本步驟。</span><span class="sxs-lookup"><span data-stu-id="f1f2e-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1f2e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1f2e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1f2e-115">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="f1f2e-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



