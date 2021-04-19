---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟1。
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 步驟1：宣告 DShowPlayer 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978027"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="ed1a8-103">步驟1：宣告 DShowPlayer 類別</span><span class="sxs-lookup"><span data-stu-id="ed1a8-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="ed1a8-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟1。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="ed1a8-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="ed1a8-106">在本教學課程中， `DShowPlayer` 類別會管理所有的 DirectShow 功能。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="ed1a8-107">此類別宣告為 folows。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-107">This class is declared as folows.</span></span>


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





<span data-ttu-id="ed1a8-108">注意：</span><span class="sxs-lookup"><span data-stu-id="ed1a8-108">Notes:</span></span>

-   <span data-ttu-id="ed1a8-109">`PlaybackState`列舉會描述物件的目前狀態 `DShowPlayer` 。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="ed1a8-110">常數 WM \_ 圖形 \_ 事件會定義私用視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="ed1a8-111">此訊息是用來通知應用程式有關篩選圖形事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="ed1a8-112">請參閱 [步驟6：處理圖形事件](step-6--handle-graph-events.md)。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="ed1a8-113">`GraphEventFN` 這是用來處理篩選圖形事件的回呼函式的指標。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="ed1a8-114">應用程式會執行這個回呼函數。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="ed1a8-115">*M \_ pVideo* 成員變數提供各種 DirectShow 影片轉譯器的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="ed1a8-116">請參閱 [步驟2：宣告 CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="ed1a8-117">在本教學課程中， [SafeRelease](../medfound/saferelease.md) 函式是用來釋放 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="ed1a8-118">下一 [步：步驟2：宣告 CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ed1a8-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed1a8-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed1a8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed1a8-120">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="ed1a8-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
