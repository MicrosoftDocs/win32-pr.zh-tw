---
description: 本主題是 DirectShow 中音訊/影片播放教學課程的步驟1。
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 步驟1：宣告 DShowPlayer 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02cbf35e9c71df9d71ab3df7cdbb3edf5d3f25bb5e77a01734f7d842fc3097f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951887"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>步驟1：宣告 DShowPlayer 類別

本主題是[DirectShow 中音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟1。 完整的程式碼會顯示在[DirectShow 播放範例](directshow-playback-example.md)的主題中。

在本教學課程中， `DShowPlayer` 類別會管理所有 DirectShow 功能。 此類別宣告為 folows。


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





注意：

-   `PlaybackState`列舉會描述物件的目前狀態 `DShowPlayer` 。
-   常數 WM \_ 圖形 \_ 事件會定義私用視窗訊息。 此訊息是用來通知應用程式有關篩選圖形事件的資訊。 請參閱[步驟6：處理 Graph 事件](step-6--handle-graph-events.md)。
-   `GraphEventFN` 這是用來處理篩選圖形事件的回呼函式的指標。 應用程式會執行這個回呼函數。
-   *m \_ pVideo* 成員變數提供各種 DirectShow 影片轉譯器的包裝函式。 請參閱 [步驟2：宣告 CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)。
-   在本教學課程中， [SafeRelease](../medfound/saferelease.md) 函式是用來釋放 COM 介面指標。

下一 [步：步驟2：宣告 CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的音訊/影片播放](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
