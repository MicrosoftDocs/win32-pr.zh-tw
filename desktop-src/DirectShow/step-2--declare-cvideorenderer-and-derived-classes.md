---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟2。
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 步驟2：宣告 CVideoRenderer 和衍生類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975383"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>步驟2：宣告 CVideoRenderer 和衍生類別

本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟2。 完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。

DirectShow 提供數種可轉譯影片的不同篩選：

-   [**增強的影片轉譯器篩選器**](enhanced-video-renderer-filter.md) (EVR) 
-   [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 
-   [影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) 

如需這些篩選之間差異的詳細資訊，請參閱 [選擇正確的影片](choosing-the-right-renderer.md)轉譯器。

在本教學課程中，會使用下列抽象類別來包裝影片轉譯器篩選器。


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



注意：

-   如果已建立影片轉譯器，則此方法會傳回 `HasVideo` **TRUE** 。
-   `AddToGraph`方法會將影片轉譯器新增至篩選圖形。
-   `FinalizeGraph`方法會完成圖形建立步驟。
-   `UpdateVideoWindow`方法會更新影片目的地矩形。
-   方法會重新 `Repaint` 繪製目前的影片畫面。
-   `DisplayModeChanged`方法會處理顯示模式變更。

本教學課程稍後會詳細說明這些方法。

接下來，宣告衍生類別以包裝三個影片轉譯器： EVR、VMR-9 和 VMR-7。

### <a name="cevr-class"></a>CEVR 類別

`CEVR`類別會管理 EVR。 它包含 EVR 的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 和 [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) 介面指標。


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>CVMR9 類別

`CVMR9`類別會管理 VMR-9。 它包含 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面的指標。


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>CVMR7 類別

`CVMR7`類別會管理 VMR-7。 它包含 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面的指標。


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



下一 [步：步驟3：建立篩選圖形](step-3--build-the-filter-graph.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 播放音訊/影片](audio-video-playback-in-directshow.md)
</dt> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> <dt>

[影片轉譯](video-rendering.md)
</dt> </dl>

 

 
