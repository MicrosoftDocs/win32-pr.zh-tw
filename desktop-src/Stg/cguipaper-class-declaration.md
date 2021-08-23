---
title: CGuiPaper 類別宣告
description: CGuiPaper 類別宣告
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d684618eea78247b94ed03223cfce45d2cc713f5507b1e290731d3451212b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663518"
---
# <a name="cguipaper-class-declaration"></a>CGuiPaper 類別宣告

以下是來自 GUIPAPER 的 **CGuiPaper** 類別宣告。


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



**CGuiPaper** 會維護繪圖紙張的目前 GUI 屬性。 成員 **m \_ crInkColor**、 **m \_ crInkWidth** 和 **m \_ WinRect** 包含目前筆墨色彩、筆墨寬度和繪製矩形的值。 **M \_ hWnd** 成員會將控制碼儲存至繪製完成的視窗。

影像的實際繪製是使用在成員 **m \_ hDC** 中保存之裝置內容的控制碼來完成。 目前繪圖畫筆的控制碼會保留在成員 **m \_ hPen** 中。 畫筆會在其色彩或寬度由使用者變更時終結並重新建立。

成員 **m \_ pCOPaperSink** 和 **m \_ dwPaperSink** 保存連接 COPaper 所需的值，以透過 [**IPaperSink**](ipapersink-methods.md) 介面接收傳入的通知。 成員 **m \_ bDirty** 會保存旗標，指出使用者已變更繪圖，且不再反映儲存在其檔案中的資料。

成員 **m \_ pIPaper** 會保存 COPaper 物件的主要介面指標。 所有 COPaper 功能都是透過這個指標來存取。

**M \_ nLockKey** 成員是用來支援與多個用戶端搭配使用的用戶端鎖定配置，以允許用戶端獨佔存取共用 COPaper 物件。 COPaper 會在 [**IPaper**](ipaper-methods.md)：：**Lock** 呼叫期間指派 **m \_ NLockKey** ，並在後續呼叫 COPaper 時，由用戶端以參數的形式傳遞。 只有當傳遞的鎖定金鑰符合上次由 COPaper 傳遞給用戶端的金鑰時，COPaper 才會在這些呼叫中執行工作。

成員 **m \_ pPapFile** 會保存 [**CPapFile**](cpapfile-class-and-methods.md) 物件的指標。 它是 c + + 物件，可封裝結構化儲存體複合檔案上的載入和儲存作業。 **CPapFile** 適用于以伺服器為基礎的基礎 COPaper 物件，以載入和儲存 COPaper 繪圖資料。

 

 




