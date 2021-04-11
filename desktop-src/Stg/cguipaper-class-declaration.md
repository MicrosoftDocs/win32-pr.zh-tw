---
title: CGuiPaper 類別宣告
description: CGuiPaper 類別宣告
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020979"
---
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="c867f-103">CGuiPaper 類別宣告</span><span class="sxs-lookup"><span data-stu-id="c867f-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="c867f-104">以下是來自 GUIPAPER 的 **CGuiPaper** 類別宣告。</span><span class="sxs-lookup"><span data-stu-id="c867f-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



<span data-ttu-id="c867f-105">**CGuiPaper** 會維護繪圖紙張的目前 GUI 屬性。</span><span class="sxs-lookup"><span data-stu-id="c867f-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="c867f-106">成員 **m \_ crInkColor**、 **m \_ crInkWidth** 和 **m \_ WinRect** 包含目前筆墨色彩、筆墨寬度和繪製矩形的值。</span><span class="sxs-lookup"><span data-stu-id="c867f-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="c867f-107">**M \_ hWnd** 成員會將控制碼儲存至繪製完成的視窗。</span><span class="sxs-lookup"><span data-stu-id="c867f-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="c867f-108">影像的實際繪製是使用在成員 **m \_ hDC** 中保存之裝置內容的控制碼來完成。</span><span class="sxs-lookup"><span data-stu-id="c867f-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="c867f-109">目前繪圖畫筆的控制碼會保留在成員 **m \_ hPen** 中。</span><span class="sxs-lookup"><span data-stu-id="c867f-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="c867f-110">畫筆會在其色彩或寬度由使用者變更時終結並重新建立。</span><span class="sxs-lookup"><span data-stu-id="c867f-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="c867f-111">成員 **m \_ pCOPaperSink** 和 **m \_ dwPaperSink** 保存連接 COPaper 所需的值，以透過 [**IPaperSink**](ipapersink-methods.md) 介面接收傳入的通知。</span><span class="sxs-lookup"><span data-stu-id="c867f-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="c867f-112">成員 **m \_ bDirty** 會保存旗標，指出使用者已變更繪圖，且不再反映儲存在其檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="c867f-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="c867f-113">成員 **m \_ pIPaper** 會保存 COPaper 物件的主要介面指標。</span><span class="sxs-lookup"><span data-stu-id="c867f-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="c867f-114">所有 COPaper 功能都是透過這個指標來存取。</span><span class="sxs-lookup"><span data-stu-id="c867f-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="c867f-115">**M \_ nLockKey** 成員是用來支援與多個用戶端搭配使用的用戶端鎖定配置，以允許用戶端獨佔存取共用 COPaper 物件。</span><span class="sxs-lookup"><span data-stu-id="c867f-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="c867f-116">COPaper 會在 [**IPaper**](ipaper-methods.md)：：**Lock** 呼叫期間指派 **m \_ NLockKey** ，並在後續呼叫 COPaper 時，由用戶端以參數的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="c867f-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="c867f-117">只有當傳遞的鎖定金鑰符合上次由 COPaper 傳遞給用戶端的金鑰時，COPaper 才會在這些呼叫中執行工作。</span><span class="sxs-lookup"><span data-stu-id="c867f-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="c867f-118">成員 **m \_ pPapFile** 會保存 [**CPapFile**](cpapfile-class-and-methods.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c867f-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="c867f-119">它是 c + + 物件，可封裝結構化儲存體複合檔案上的載入和儲存作業。</span><span class="sxs-lookup"><span data-stu-id="c867f-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="c867f-120">**CPapFile** 適用于以伺服器為基礎的基礎 COPaper 物件，以載入和儲存 COPaper 繪圖資料。</span><span class="sxs-lookup"><span data-stu-id="c867f-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




