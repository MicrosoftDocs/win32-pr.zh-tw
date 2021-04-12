---
title: 在 Windows 應用程式中裝載 Windows Media Player 控制項
description: 在 Windows 應用程式中裝載 Windows Media Player 控制項
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，以 Windows 為基礎的程式
- Windows Media Player 物件模型，以 Windows 為基礎的程式
- 物件模型，以 Windows 為基礎的程式
- Windows Media Player 行動裝置、以 Windows 為基礎的程式
- Windows Media Player ActiveX 控制項，以 Windows 為基礎的程式
- Windows Media Player 的行動 ActiveX 控制項，以 Windows 為基礎的程式
- ActiveX 控制項，以 Windows 為基礎的程式
- 以 Windows 為基礎的程式內嵌
- 內嵌、以 Windows 為基礎的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301604"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>在 Windows 應用程式中裝載 Windows Media Player 控制項

若要使用 Windows Media Player 的 ActiveX 控制項 (包括 Windows 程式) 的使用者介面，您必須提供 ActiveX 控制項容器。 ATL 提供 **CAxWindow** 類別來提供 ActiveX 主控制項視窗功能。

若要使用 **CAxWindow** 類別裝載 Windows Media Player 控制項，請遵循下列步驟：

1.  包含下列標頭：
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  宣告成員變數，如下所示：
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  當您的應用程式視窗建立時，請呼叫 **AtlAxWinInit**，這在使用 ATL ActiveX 主控制項視窗時是必要的。
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  宣告傳回碼的區域變數，並包含主機視窗介面的指標：
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  建立主機視窗：
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  取出主機視窗介面指標：
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  使用類別識別碼在主機視窗中建立 Windows Media Player 控制項：
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  取出 **IWMPPlayer** 介面指標：
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

當您撰寫自己的程式碼時，請務必檢查每個 **HRESULT** 傳回碼是否有錯誤。

如需示範如何使用 **CAxWindow** 類別裝載 Windows Media Player ActiveX 控制項的完整範例，請參閱 WMPHost 範例。

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>在 Windows CE 中裝載 Windows Media Player 10 行動裝置控制項

開發 Windows Media Player 10 行動裝置版控制項的 Windows CE 型應用程式時，必須安裝 Microsoft eMbedded Visual C++ 4.0 與 Pocket PC 2003 SDK 或 Smartphone 2003 SDK。 此外，與適用于 Windows 的 ATL 不同的是，適用于 Windows CE 的 ATL 不支援單元執行緒模型。 因此，您必須在 ATL 專案中尋找所有單元執行緒的實例，並將其變更為使用自由執行緒。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例**](samples.md)
</dt> <dt>

[**在 c + + 程式中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




