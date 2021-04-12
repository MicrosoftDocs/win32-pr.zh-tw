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
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="be8f6-119">在 Windows 應用程式中裝載 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="be8f6-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="be8f6-120">若要使用 Windows Media Player 的 ActiveX 控制項 (包括 Windows 程式) 的使用者介面，您必須提供 ActiveX 控制項容器。</span><span class="sxs-lookup"><span data-stu-id="be8f6-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="be8f6-121">ATL 提供 **CAxWindow** 類別來提供 ActiveX 主控制項視窗功能。</span><span class="sxs-lookup"><span data-stu-id="be8f6-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="be8f6-122">若要使用 **CAxWindow** 類別裝載 Windows Media Player 控制項，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="be8f6-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="be8f6-123">包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="be8f6-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="be8f6-124">宣告成員變數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="be8f6-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="be8f6-125">當您的應用程式視窗建立時，請呼叫 **AtlAxWinInit**，這在使用 ATL ActiveX 主控制項視窗時是必要的。</span><span class="sxs-lookup"><span data-stu-id="be8f6-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="be8f6-126">宣告傳回碼的區域變數，並包含主機視窗介面的指標：</span><span class="sxs-lookup"><span data-stu-id="be8f6-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="be8f6-127">建立主機視窗：</span><span class="sxs-lookup"><span data-stu-id="be8f6-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="be8f6-128">取出主機視窗介面指標：</span><span class="sxs-lookup"><span data-stu-id="be8f6-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="be8f6-129">使用類別識別碼在主機視窗中建立 Windows Media Player 控制項：</span><span class="sxs-lookup"><span data-stu-id="be8f6-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="be8f6-130">取出 **IWMPPlayer** 介面指標：</span><span class="sxs-lookup"><span data-stu-id="be8f6-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="be8f6-131">當您撰寫自己的程式碼時，請務必檢查每個 **HRESULT** 傳回碼是否有錯誤。</span><span class="sxs-lookup"><span data-stu-id="be8f6-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="be8f6-132">如需示範如何使用 **CAxWindow** 類別裝載 Windows Media Player ActiveX 控制項的完整範例，請參閱 WMPHost 範例。</span><span class="sxs-lookup"><span data-stu-id="be8f6-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="be8f6-133">在 Windows CE 中裝載 Windows Media Player 10 行動裝置控制項</span><span class="sxs-lookup"><span data-stu-id="be8f6-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="be8f6-134">開發 Windows Media Player 10 行動裝置版控制項的 Windows CE 型應用程式時，必須安裝 Microsoft eMbedded Visual C++ 4.0 與 Pocket PC 2003 SDK 或 Smartphone 2003 SDK。</span><span class="sxs-lookup"><span data-stu-id="be8f6-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="be8f6-135">此外，與適用于 Windows 的 ATL 不同的是，適用于 Windows CE 的 ATL 不支援單元執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="be8f6-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="be8f6-136">因此，您必須在 ATL 專案中尋找所有單元執行緒的實例，並將其變更為使用自由執行緒。</span><span class="sxs-lookup"><span data-stu-id="be8f6-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be8f6-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="be8f6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be8f6-138">**範例**</span><span class="sxs-lookup"><span data-stu-id="be8f6-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="be8f6-139">**在 c + + 程式中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="be8f6-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




