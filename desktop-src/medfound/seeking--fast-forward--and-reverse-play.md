---
description: 本主題說明使用媒體會話進行播放時，管理搜尋和速率變更的範例程式碼。
ms.assetid: 50bf4c05-99c0-4cf0-aaca-8ee717cafd12
title: 搜尋、向前快轉及反向播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c42e4ab2bbf5bd3ac1057ce4bb0e09fceddc44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973911"
---
# <a name="seeking-fast-forward-and-reverse-play"></a><span data-ttu-id="25570-103">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="25570-103">Seeking, Fast Forward, and Reverse Play</span></span>

<span data-ttu-id="25570-104">本主題說明使用 [媒體會話](media-session.md) 進行播放時，管理搜尋和速率變更的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="25570-104">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span>

<span data-ttu-id="25570-105">使用媒體會話進行播放時，應用程式可以搜尋並變更播放速率，如下所示：</span><span class="sxs-lookup"><span data-stu-id="25570-105">When using the Media Session for playback, an application can seek and change the playback rate as follows:</span></span>

-   <span data-ttu-id="25570-106">若要搜尋，請呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 並指定搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="25570-106">To seek, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) and specify the seek position.</span></span>
-   <span data-ttu-id="25570-107">若要變更播放速率，請使用 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面，如 [速率控制](rate-control.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="25570-107">To change the playback rate, use the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface as described in [Rate Control](rate-control.md).</span></span>
-   <span data-ttu-id="25570-108">若要在搜尋時取得更新的影片畫面，請在呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)之前，將播放速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="25570-108">To get updated video frames while seeking, set the playback rate to zero before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="25570-109">這項作業稱為「 *清理*」。</span><span class="sxs-lookup"><span data-stu-id="25570-109">This operation is called *scrubbing*.</span></span> <span data-ttu-id="25570-110"> (瞭解 [如何執行清理](how-to-perform-scrubbing.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="25570-110">(See [How to Perform Scrubbing](how-to-perform-scrubbing.md).)</span></span>

<span data-ttu-id="25570-111">不過，若要建立最佳的使用者體驗，您必須考慮下列行為：</span><span class="sxs-lookup"><span data-stu-id="25570-111">To create the best user experience, however, you must take the following behaviors into account:</span></span>

-   <span data-ttu-id="25570-112">搜尋是非同步，而媒體會話會將 FIFO 佇列上的所有搜尋要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="25570-112">Seeking is asynchronous, and the Media Session queues all seek requests on a FIFO queue.</span></span> <span data-ttu-id="25570-113">如果您提交多個搜尋要求，UI 可能會在實際播放狀態之前執行。</span><span class="sxs-lookup"><span data-stu-id="25570-113">If you submit multiple seek requests, the UI might run ahead of the actual playback state.</span></span> <span data-ttu-id="25570-114">例如，假設您的應用程式會實行搜尋列。</span><span class="sxs-lookup"><span data-stu-id="25570-114">For example, suppose your application implements a seek bar.</span></span> <span data-ttu-id="25570-115">如果使用者向前及向後拖曳搜尋列，則在執行正向搜尋時可能會有延遲。</span><span class="sxs-lookup"><span data-stu-id="25570-115">If the user drags the seek bar forward and backward, there might be a lag while the forward seeks are executed.</span></span> <span data-ttu-id="25570-116">進行搜尋時，您應該快取使用者的搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="25570-116">While a seek is in progress, you should cache the user's seek requests.</span></span> <span data-ttu-id="25570-117">當目前的搜尋作業完成時，請提交使用者最新的搜尋要求，並捨棄其他要求。</span><span class="sxs-lookup"><span data-stu-id="25570-117">When the current seek operation completes, submit the user's most recent seek request and discard the others.</span></span>
-   <span data-ttu-id="25570-118">某些傳輸狀態不允許某些速率轉換。</span><span class="sxs-lookup"><span data-stu-id="25570-118">Some rate transitions are not allowed in some transport states.</span></span> <span data-ttu-id="25570-119">例如，播放時不允許從向前播放切換至反向播放。</span><span class="sxs-lookup"><span data-stu-id="25570-119">For example, switching from forward playback to reverse playback is not allowed while playing.</span></span> <span data-ttu-id="25570-120">支援的轉換如 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)所述。</span><span class="sxs-lookup"><span data-stu-id="25570-120">The supported transitions are described in [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).</span></span> <span data-ttu-id="25570-121">速率變更也是非同步。</span><span class="sxs-lookup"><span data-stu-id="25570-121">Rate changes are also asynchronous.</span></span>

<span data-ttu-id="25570-122">下列 helper 類別可以用來管理搜尋要求和速率變更。</span><span class="sxs-lookup"><span data-stu-id="25570-122">The following helper class can be used to manage seek requests and rate changes.</span></span> <span data-ttu-id="25570-123">非同步作業暫止時，類別會快取任何搜尋或速率變更要求。</span><span class="sxs-lookup"><span data-stu-id="25570-123">While an asynchronous operation is pending, the class caches any seek or rate-change requests.</span></span> <span data-ttu-id="25570-124">當目前的作業完成時，類別會提交最近的要求（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="25570-124">When the current operation completes, the class submits the most recent request, if any.</span></span> <span data-ttu-id="25570-125">此類別也會管理傳輸狀態，以避免不正確速率變更。</span><span class="sxs-lookup"><span data-stu-id="25570-125">The class also manages the transport state to avoid invalid rate changes.</span></span>

<span data-ttu-id="25570-126">以下是 PlayerSeeking 類別的宣告。</span><span class="sxs-lookup"><span data-stu-id="25570-126">Here is the declaration of the PlayerSeeking class.</span></span>


```C++
// Implements seeking and rate control functionality.

/*
    Usage:

    - Call SetTopology when you get the MF_TOPOSTATUS_READY session event.
    - Call SessionEvent for each session event.
    - Call Clear before closing the Media Session.
    - To coordinate rate-change requests with transport state, delegate all 
      stop, pause, and play commands to the PlayerSeeking class.

*/

class PlayerSeeking 
{
    class CritSec
    {
    private:
        CRITICAL_SECTION m_criticalSection;
    public:
        CritSec()
        {
            InitializeCriticalSection(&m_criticalSection);
        }
        ~CritSec()
        {
            DeleteCriticalSection(&m_criticalSection);
        }
        void Lock()
        {
            EnterCriticalSection(&m_criticalSection);
        }
        void Unlock()
        {
            LeaveCriticalSection(&m_criticalSection);
        }
    };

    class AutoLock
    {
    private:
        CritSec *m_pCriticalSection;
    public:
        AutoLock(CritSec& crit)
        {
            m_pCriticalSection = &crit;
            m_pCriticalSection->Lock();
        }
        ~AutoLock()
        {
            m_pCriticalSection->Unlock();
        }
    };

public:

    PlayerSeeking();
    virtual ~PlayerSeeking();

    HRESULT SetTopology(IMFMediaSession *pSession, IMFTopology *pTopology);
    HRESULT Clear();
    HRESULT SessionEvent(MediaEventType type, HRESULT hrStatus, IMFMediaEvent *pEvent);

    HRESULT CanSeek(BOOL *pbCanSeek);
    HRESULT GetDuration(MFTIME *phnsDuration);
    HRESULT GetCurrentPosition(MFTIME *phnsPosition);
    HRESULT SetPosition(MFTIME hnsPosition);

    HRESULT CanScrub(BOOL *pbCanScrub);
    HRESULT Scrub(BOOL bScrub);

    HRESULT CanFastForward(BOOL *pbCanFF);
    HRESULT CanRewind(BOOL *pbCanRewind);
    HRESULT SetRate(float fRate);
    HRESULT FastForward();
    HRESULT Rewind();

    HRESULT Start();
    HRESULT Pause();
    HRESULT Stop();

private:

    enum Command
    {
        CmdNone = 0,
        CmdStop,
        CmdStart,
        CmdPause,
        CmdSeek,
    };

    HRESULT SetPositionInternal(const MFTIME &hnsPosition);
    HRESULT CommitRateChange(float fRate, BOOL bThin);
    float   GetNominalRate();

    HRESULT OnSessionStart(HRESULT hr);
    HRESULT OnSessionStop(HRESULT hr);
    HRESULT OnSessionPause(HRESULT hr);
    HRESULT OnSessionEnded(HRESULT hr);

    HRESULT UpdatePendingCommands(Command cmd);

private:

    // Describes the current or requested state, with respect to seeking and 
    // playback rate.
    struct SeekState
    {
        Command command;
        float   fRate;      // Playback rate
        BOOL    bThin;      // Thinned playback?
        MFTIME  hnsStart;   // Start position
    };

    BOOL        m_bPending;     // Is a request pending?

    SeekState   m_state;        // Current nominal state.
    SeekState   m_request;      // Pending request.

    CritSec     m_critsec;      // Protects the seeking and rate-change states.

    DWORD       m_caps;         // Session caps.
    BOOL        m_bCanScrub;    // Does the current session support rate = 0.

    MFTIME      m_hnsDuration;  // Duration of the current presentation.
    float       m_fPrevRate;

    IMFMediaSession         *m_pSession;
    IMFRateControl          *m_pRate;
    IMFRateSupport          *m_pRateSupport;
    IMFPresentationClock    *m_pClock;
};
```



<span data-ttu-id="25570-127">以下是 PlayerSeeking 類別的實作為。</span><span class="sxs-lookup"><span data-stu-id="25570-127">Here is the implementation of the PlayerSeeking class.</span></span>


```C++
#include <assert.h>
#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mferror.h>
#include "seeking.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

#define CMD_PENDING      0x01
#define CMD_PENDING_SEEK 0x02
#define CMD_PENDING_RATE 0x04

// Given a topology, returns a pointer to the presentation descriptor.

HRESULT GetPresentationDescriptorFromTopology(
    IMFTopology *pTopology,
    IMFPresentationDescriptor **ppPD
    )
{
    HRESULT hr = S_OK;

    IMFCollection *pCollection = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;
    IMFPresentationDescriptor *pPD = NULL;

    // Get the collection of source nodes from the topology.
    hr = pTopology->GetSourceNodeCollection(&pCollection);
    if (FAILED(hr))
    {
        goto done;
    }

    // Any of the source nodes should have the PD, so take the first
    // object in the collection.

    hr = pCollection->GetElement(0, &pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pUnk->QueryInterface(IID_PPV_ARGS(&pNode));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the PD, which is stored as an attribute.
    hr = pNode->GetUnknown(
        MF_TOPONODE_PRESENTATION_DESCRIPTOR, IID_PPV_ARGS(&pPD));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppPD = pPD;
    (*ppPD)->AddRef();

done:
    SafeRelease(&pCollection);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    SafeRelease(&pPD);
    return hr;
}


PlayerSeeking::PlayerSeeking()
    : m_pClock(NULL),
      m_pSession(NULL),
      m_pRate(NULL),
      m_pRateSupport(NULL),
      m_bPending(FALSE)
{
    Clear();
}

PlayerSeeking::~PlayerSeeking()
{
    SafeRelease(&m_pClock);
    SafeRelease(&m_pSession);
    SafeRelease(&m_pRate);
    SafeRelease(&m_pRateSupport);
}

// Clears any resources for the current topology.

HRESULT PlayerSeeking::Clear()
{
    m_caps = 0;
    m_bCanScrub = FALSE;

    m_hnsDuration = 0;
    m_fPrevRate = 1.0f;

    m_bPending = FALSE;

    SafeRelease(&m_pClock);
    SafeRelease(&m_pSession);
    SafeRelease(&m_pRate);
    SafeRelease(&m_pRateSupport);

    ZeroMemory(&m_state, sizeof(m_state));
    m_state.command = CmdStop;
    m_state.fRate = 1.0f;

    ZeroMemory(&m_request, sizeof(m_request));
    m_request.command = CmdNone;
    m_request.fRate = 1.0f;

    return S_OK;
}


// Call when the full playback topology is ready.

HRESULT PlayerSeeking::SetTopology(IMFMediaSession *pSession, IMFTopology *pTopology)
{
    HRESULT hr = S_OK;
    HRESULT hrTmp = S_OK;   // For non-critical failures.

    IMFClock *pClock = NULL;
    IMFPresentationDescriptor *pPD = NULL;

    Clear();

    // Get the session capabilities.
    hr = pSession->GetSessionCapabilities(&m_caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the presentation descriptor from the topology.
    hr = GetPresentationDescriptorFromTopology(pTopology, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the duration from the presentation descriptor (optional)
    (void)pPD->GetUINT64(MF_PD_DURATION, (UINT64*)&m_hnsDuration);

    // Get the presentation clock (optional)
    hrTmp = pSession->GetClock(&pClock);
    if (SUCCEEDED(hrTmp))
    {
        hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the rate control interface (optional)
    hrTmp = MFGetService(
        pSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&m_pRate));

    // Get the rate support interface (optional)
    if (SUCCEEDED(hrTmp))
    {
        hrTmp = MFGetService(
            pSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&m_pRateSupport));
    }
    if (SUCCEEDED(hrTmp))
    {
        // Check if rate 0 (scrubbing) is supported.
        hrTmp = m_pRateSupport->IsRateSupported(TRUE, 0, NULL);
    }
    if (SUCCEEDED(hrTmp))
    {
        m_bCanScrub = TRUE;
    }

    // if m_pRate is NULL, m_bCanScrub must be FALSE.
    assert(m_pRate || !m_bCanScrub); 

    // Cache a pointer to the session.
    m_pSession = pSession;
    m_pSession->AddRef();

done:
    SafeRelease(&pPD);
    SafeRelease(&pClock);
    return hr;
}

// Call when media session fires an event.

HRESULT PlayerSeeking::SessionEvent(
    MediaEventType type, 
    HRESULT hrStatus, 
    IMFMediaEvent *pEvent
    )
{
    PROPVARIANT var;
    HRESULT hr = S_OK;

    switch (type)
    {
    case MESessionStarted:
        OnSessionStart(hrStatus);
        break;

    case MESessionStopped:
        OnSessionStop(hrStatus);
        break;

    case MESessionPaused:
        OnSessionPause(hrStatus);
        break;

    case MESessionRateChanged:
        // If the rate change succeeded, we've already got the rate
        // cached. If it failed, try to get the actual rate.
        if (FAILED(hrStatus))
        {
            PropVariantInit(&var);

            hr = pEvent->GetValue(&var);

            if (SUCCEEDED(hr) && (var.vt == VT_R4))
            {
                m_state.fRate = var.fltVal;
            }
        }
        break;

    case MESessionEnded:
        OnSessionEnded(hrStatus);
        break;

    case MESessionCapabilitiesChanged:
        // The session capabilities changed. Get the updated capabilities.
        m_caps = MFGetAttributeUINT32(pEvent, MF_EVENT_SESSIONCAPS, m_caps);
        break;
    }
    return S_OK;
}


// Starts playback.

HRESULT PlayerSeeking::Start()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, start the media session.
    if (m_bPending)
    {
       m_request.command = CmdStart;
    }
    else
    {
        PROPVARIANT varStart;
        PropVariantInit(&varStart);

        hr =  m_pSession->Start(NULL, &varStart);

        m_state.command = CmdStart;
        m_bPending = CMD_PENDING;
    }
    return hr;
}


// Pauses playback.

HRESULT PlayerSeeking::Pause()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, pause the media session.
    if (m_bPending)
    {
        m_request.command = CmdPause;
    }
    else
    {
        hr =  m_pSession->Pause();

        m_state.command = CmdPause;
        m_bPending = CMD_PENDING;
    }
    return hr;
}


// Stops playback.

HRESULT PlayerSeeking::Stop()
{
    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    // If another operation is pending, cache the request.
    // Otherwise, stop the media session.
    if (m_bPending)
    {
        m_request.command = CmdStop;
    }
    else
    {
        hr =  m_pSession->Stop();

        m_state.command = CmdStop;
        m_bPending = CMD_PENDING;
    }
    return hr;
}

// Queries whether the current session supports seeking.

HRESULT PlayerSeeking::CanSeek(BOOL *pbCanSeek)
{
    if (pbCanSeek == NULL)
    {
        return E_POINTER;
    }

    // Note: The MFSESSIONCAP_SEEK flag is sufficient for seeking. However, to
    // implement a seek bar, an application also needs the duration (to get 
    // the valid range) and a presentation clock (to get the current position).

    *pbCanSeek = (
        ((m_caps & MFSESSIONCAP_SEEK) == MFSESSIONCAP_SEEK) &&
        (m_hnsDuration > 0) &&
        (m_pClock != NULL)
        );

    return S_OK;
}


// Gets the duration of the current presentation.

HRESULT PlayerSeeking::GetDuration(MFTIME *phnsDuration)
{
    if (phnsDuration == NULL)
    {
        return E_POINTER;
    }

    *phnsDuration = m_hnsDuration;

    if (m_hnsDuration == 0)
    {
        return MF_E_NO_DURATION;
    }
    else
    {
        return S_OK;
    }
}

// Gets the current playback position.

HRESULT PlayerSeeking::GetCurrentPosition(MFTIME *phnsPosition)
{
    if (phnsPosition == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    AutoLock lock(m_critsec);

    if (m_pClock == NULL)
    {
        return MF_E_NO_CLOCK;
    }

    // Return, in order:
    // 1. Cached seek request (nominal position).
    // 2. Pending seek operation (nominal position).
    // 3. Presentation time (actual position).

    if (m_request.command == CmdSeek)
    {
        *phnsPosition = m_request.hnsStart;
    }
    else if (m_bPending & CMD_PENDING_SEEK)
    {
        *phnsPosition = m_state.hnsStart;
    }
    else
    {
        hr = m_pClock->GetTime(phnsPosition);
    }

    return hr;
}


// Sets the current playback position.

HRESULT PlayerSeeking::SetPosition(MFTIME hnsPosition)
{
    AutoLock lock(m_critsec);

    HRESULT hr = S_OK;

    if (m_bPending)
    {
        // Currently seeking or changing rates, so cache this request.
        m_request.command = CmdSeek;
        m_request.hnsStart = hnsPosition;
    }
    else
    {
        hr = SetPositionInternal(hnsPosition);
    }

    return hr;
}


// Queries whether the current session supports scrubbing.

HRESULT PlayerSeeking::CanScrub(BOOL *pbCanScrub)
{
    if (pbCanScrub == NULL)
    {
        return E_POINTER;
    }

    *pbCanScrub = m_bCanScrub;
    return S_OK;
}


// Enables or disables scrubbing.

HRESULT PlayerSeeking::Scrub(BOOL bScrub)
{
    // Scrubbing is implemented as rate = 0.

    AutoLock lock(m_critsec);

    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (!m_bCanScrub)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;

    if (bScrub)
    {
        // Enter scrubbing mode. Cache the current rate.

        if (GetNominalRate() != 0)
        {
            m_fPrevRate = m_state.fRate;
        }

        hr = SetRate(0.0f);
    }
    else
    {
        // Leaving scrubbing mode. Restore the old rate.

        if (GetNominalRate() == 0)
        {
            hr = SetRate(m_fPrevRate);
        }
    }

    return hr;
}


// Queries whether the current session supports fast-forward.

HRESULT PlayerSeeking::CanFastForward(BOOL *pbCanFF)
{
    if (pbCanFF == NULL)
    {
        return E_POINTER;
    }

    *pbCanFF = 
        ((m_caps & MFSESSIONCAP_RATE_FORWARD) == MFSESSIONCAP_RATE_FORWARD);
    return S_OK;
}


// Queries whether the current session supports rewind (reverse play).

HRESULT PlayerSeeking::CanRewind(BOOL *pbCanRewind)
{
    if (pbCanRewind == NULL)
    {
        return E_POINTER;
    }

    *pbCanRewind = 
        ((m_caps & MFSESSIONCAP_RATE_REVERSE) == MFSESSIONCAP_RATE_REVERSE);
    return S_OK;
}


// Switches to fast-forward playback, as follows:
// - If the current rate is < 0 (reverse play), switch to 1x speed.
// - Otherwise, double the current playback rate.
//
// Note: This method is for convenience; the application can also call SetRate.

HRESULT PlayerSeeking::FastForward()
{
    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;
    float   fTarget = GetNominalRate() * 2;

    if (fTarget <= 0.0f)
    {
        fTarget = 1.0f;
    }

    hr = SetRate(fTarget);

    return hr;
}


// Switches to reverse playback, as follows:
// - If the current rate is > 0 (forward playback), switch to -1x speed.
// - Otherwise, double the current (reverse) playback rate.
//
// Note: This method is for convenience; the application can also call SetRate.

HRESULT PlayerSeeking::Rewind()
{
    if (!m_pRate)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;
    float   fTarget = GetNominalRate() * 2;

    if (fTarget >= 0.0f)
    {
        fTarget = -1.0f;
    }

    hr = SetRate(fTarget);

    return hr;
}


// Sets the playback rate.

HRESULT PlayerSeeking::SetRate(float fRate)
{
    HRESULT hr = S_OK;
    BOOL bThin = FALSE;

    AutoLock lock(m_critsec);

    if (fRate == GetNominalRate())
    {
        return S_OK; // no-op
    }

    if (m_pRateSupport == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Check if this rate is supported. Try non-thinned playback first,
    // then fall back to thinned playback.

    hr = m_pRateSupport->IsRateSupported(FALSE, fRate, NULL);

    if (FAILED(hr))
    {
        bThin = TRUE;
        hr = m_pRateSupport->IsRateSupported(TRUE, fRate, NULL);
    }

    if (FAILED(hr))
    {
        // Unsupported rate.
        return hr;
    }

    // If there is an operation pending, cache the request.
    if (m_bPending)
    {
        m_request.fRate = fRate;
        m_request.bThin = bThin;

        // Remember the current transport state (play, paused, etc), so that we
        // can restore it after the rate change, if necessary. However, if 
        // anothercommand is already pending, that one takes precedent.

        if (m_request.command == CmdNone)
        {
            m_request.command = m_state.command;
        }

    }
    else
    {
        // No pending operation. Commit the new rate.
        hr  = CommitRateChange(fRate, bThin);
    }

    return hr;

}

// Sets the playback position.

HRESULT PlayerSeeking::SetPositionInternal(const MFTIME &hnsPosition)
{
    assert (!m_bPending);

    if (m_pSession == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    HRESULT hr = S_OK;

    PROPVARIANT varStart;
    varStart.vt = VT_I8;
    varStart.hVal.QuadPart = hnsPosition;

    hr =  m_pSession->Start(NULL, &varStart);

    if (SUCCEEDED(hr))
    {
        // Store the pending state.
        m_state.command = CmdStart;
        m_state.hnsStart = hnsPosition;
        m_bPending = CMD_PENDING_SEEK;
    }
    return hr;
}




// Sets the playback rate.

HRESULT PlayerSeeking::CommitRateChange(float fRate, BOOL bThin)
{
    assert (!m_bPending);

    // Caller holds the lock.

    HRESULT hr = S_OK;
    MFTIME  hnsSystemTime = 0;
    MFTIME  hnsClockTime = 0;

    Command cmdNow = m_state.command;

    IMFClock *pClock = NULL;

    // Allowed rate transitions:

    // Positive <-> negative:   Stopped
    // Negative <-> zero:       Stopped
    // Postive <-> zero:        Paused or stopped

    if ((fRate > 0 && m_state.fRate <= 0) || (fRate < 0 && m_state.fRate >= 0))
    {
        // Transition to stopped.
        if (cmdNow == CmdStart)
        {
            // Get the current clock position. This will be the restart time.
            hr = m_pSession->GetClock(&pClock);
            if (FAILED(hr))
            {
                goto done;
            }

            (void)pClock->GetCorrelatedTime(0, &hnsClockTime, &hnsSystemTime);

            assert(hnsSystemTime != 0);

            // Stop and set the rate
            hr = Stop();
            if (FAILED(hr))
            {
                goto done;
            }

            // Cache Request: Restart from stop.
            m_request.command = CmdSeek;
            m_request.hnsStart = hnsClockTime;
        }
        else if (cmdNow == CmdPause)
        {
            // The current state is paused.

            // For this rate change, the session must be stopped. However, the 
            // session cannot transition back from stopped to paused. 
            // Therefore, this rate transition is not supported while paused.

            hr = MF_E_UNSUPPORTED_STATE_TRANSITION;
            goto done;
        }
    }
    else if (fRate == 0 && m_state.fRate != 0)
    {
        if (cmdNow != CmdPause)
        {
           // Transition to paused.

            // This transisition requires the paused state.

            // Pause and set the rate.
            hr = Pause();
            if (FAILED(hr))
            {
                goto done;
            }

            // Request: Switch back to current state.
            m_request.command = cmdNow;
        }
    }

    // Set the rate.
    hr = m_pRate->SetRate(bThin, fRate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Adjust our current rate and requested rate.
    m_request.fRate = m_state.fRate = fRate;

done:
    SafeRelease(&pClock);
    return hr;
}


float PlayerSeeking::GetNominalRate()
{
    return m_request.fRate;
}


// Called when playback starts or restarts.

HRESULT PlayerSeeking::OnSessionStart(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    // The Media Session completed a start/seek operation. Check if there
    // is another seek request pending.
    UpdatePendingCommands(CmdStart);

    return hr;
}


// Called when playback stops.

HRESULT PlayerSeeking::OnSessionStop(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    // The Media Session completed a transition to stopped. This might occur
    // because we are changing playback direction (forward/rewind). Check if
    // there is a pending rate-change request.

    UpdatePendingCommands(CmdStop);

    return hr;
}


// Called when playback pauses.

HRESULT PlayerSeeking::OnSessionPause(HRESULT hrStatus)
{
    HRESULT hr = S_OK;

    if (FAILED(hrStatus))
    {
        return hrStatus;
    }

    hr = UpdatePendingCommands(CmdPause);

    return hr;
}



// Called when the session ends.

HRESULT PlayerSeeking::OnSessionEnded(HRESULT hr)
{
    // After the session ends, playback starts from position zero. But if the
    // current playback rate is reversed, playback would end immediately 
    // (reversing from position 0). Therefore, reset the rate to 1x.

    if (GetNominalRate() < 0.0f)
    {
        m_state.command = CmdStop;

        hr = CommitRateChange(1.0f, FALSE);
    }

    return hr;
}


// Called after an operation completes.
// This method executes any cached requests.

HRESULT PlayerSeeking::UpdatePendingCommands(Command cmd)
{
    HRESULT hr = S_OK;

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    AutoLock lock(m_critsec);

    if (m_bPending && m_state.command == cmd)
    {
        m_bPending = FALSE;

        // The current pending command has completed.

        // First look for rate changes.
        if (m_request.fRate != m_state.fRate)
        {
            hr = CommitRateChange(m_request.fRate, m_request.bThin);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Now look for seek requests.
        if (!m_bPending)
        {
            switch (m_request.command)
            {
            case CmdNone:
                // Nothing to do.
                break;

            case CmdStart:
                Start();
                break;

            case CmdPause:
                Pause();
                break;

            case CmdStop:
                Stop();
                break;

            case CmdSeek:
                SetPositionInternal(m_request.hnsStart);
                break;
            }
            m_request.command = CmdNone;
        }
    }

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="25570-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="25570-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25570-129">速率控制</span><span class="sxs-lookup"><span data-stu-id="25570-129">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="25570-130">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="25570-130">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



