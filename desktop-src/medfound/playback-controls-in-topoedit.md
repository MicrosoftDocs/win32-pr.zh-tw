---
description: TopoEdit 中的播放控制項
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: TopoEdit 中的播放控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562185"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="2f5b7-103">TopoEdit 中的播放控制項</span><span class="sxs-lookup"><span data-stu-id="2f5b7-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="2f5b7-104">拓撲解決之後，它會排入媒體會話以供播放。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="2f5b7-105">TopoEdit 提供在媒體會話上變更拓撲狀態的傳輸控制。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="2f5b7-106">下表顯示功能表/工具列命令和每個作業的對等媒體基礎方法。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="2f5b7-107">功能表/工具列命令</span><span class="sxs-lookup"><span data-stu-id="2f5b7-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="2f5b7-108">媒體基礎方法</span><span class="sxs-lookup"><span data-stu-id="2f5b7-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2f5b7-109">在 [**控制項**] 功能表上，按一下 [**播放**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**播放**] 按鈕 (下圖) 所示。 \[[播放] 按鈕的換行 \] ![ 螢幕擷取畫面](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f5b7-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="2f5b7-110">**IMFMediaSession：： Start**</span><span class="sxs-lookup"><span data-stu-id="2f5b7-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="2f5b7-111">在 [**控制項**] 功能表上，按一下 [**停止**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**停止**] 按鈕 (如下圖所示) 。 \[\] ![ [停止] 按鈕的換行螢幕擷取畫面](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f5b7-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="2f5b7-112">**IMFMediaSession：： Stop**</span><span class="sxs-lookup"><span data-stu-id="2f5b7-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="2f5b7-113">在 [**控制項**] 功能表上，按一下 [**暫停**]。 \[換行 \] 或換行的方式， \[ \] 請按一下工具列上的 [**暫停**] 按鈕 (如下圖所示) 。 \[\] ![ [暫停] 按鈕的換行螢幕擷取畫面](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="2f5b7-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="2f5b7-114">**IMFMediaSession：:P ause**</span><span class="sxs-lookup"><span data-stu-id="2f5b7-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="2f5b7-115">如需使用媒體基礎 Api 以程式設計方式控制播放的相關資訊，請參閱 [如何控制呈現狀態](how-to-control-presentation-states.md)。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="2f5b7-116">尋求</span><span class="sxs-lookup"><span data-stu-id="2f5b7-116">Seeking</span></span>

<span data-ttu-id="2f5b7-117">如果拓撲是可搜尋的，您可以使用下圖所示的搜尋列 (進行搜尋，) 指定拓撲的時間軸中的位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![搜尋列的螢幕擷取畫面](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="2f5b7-119">如果媒體來源是可搜尋的，則 [停止] 命令也會將拓撲搜尋回資料流程的開頭。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="2f5b7-120">變更播放速率</span><span class="sxs-lookup"><span data-stu-id="2f5b7-120">Changing the Playback Rate</span></span>

<span data-ttu-id="2f5b7-121">如果拓撲的基礎媒體來源支援多種播放率，您可以使用費率列來變更播放速率。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="2f5b7-122">若要在媒體會話上向前快轉拓撲，請將滑杆向右拖曳，以增加速率，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![費率列的螢幕擷取畫面](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="2f5b7-124">在此版本中，TopoEdit 僅支援正數費率。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="2f5b7-125">不支援反向播放。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="2f5b7-126">如需使用媒體基礎 Api 以程式設計方式變更播放速率的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="2f5b7-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f5b7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f5b7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f5b7-128">TopoEdit 功能表</span><span class="sxs-lookup"><span data-stu-id="2f5b7-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="2f5b7-129">TopoEdit 工具列</span><span class="sxs-lookup"><span data-stu-id="2f5b7-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="2f5b7-130">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2f5b7-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



