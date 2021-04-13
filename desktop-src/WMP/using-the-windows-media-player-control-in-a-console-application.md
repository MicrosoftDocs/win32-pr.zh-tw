---
title: 在主控台應用程式中使用 Windows Media Player 控制項
description: 在主控台應用程式中使用 Windows Media Player 控制項
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，主控台應用程式
- Windows Media Player 物件模型，主控台應用程式
- 物件模型，主控台應用程式
- Windows Media Player 行動裝置、主控台應用程式
- Windows Media Player ActiveX 控制項，主控台應用程式
- Windows Media Player 的行動 ActiveX 控制項，主控台應用程式
- ActiveX 控制項，主控台應用程式
- 主控台應用程式內嵌
- 內嵌，主控台應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301231"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a><span data-ttu-id="fcbc0-119">在主控台應用程式中使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="fcbc0-119">Using the Windows Media Player Control in a Console Application</span></span>

<span data-ttu-id="fcbc0-120">您可以使用 **CoCreateInstance** 直接建立 Windows Media Player COM 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="fcbc0-120">You can create an instance of the Windows Media Player COM object directly by using **CoCreateInstance**.</span></span> <span data-ttu-id="fcbc0-121">當您這樣做時， **Player** 物件就不會顯示任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="fcbc0-121">When you do this, the **Player** object displays no user interface.</span></span> <span data-ttu-id="fcbc0-122">不過，對於不需要使用者介面的工作（例如，使用程式庫、播放數位音訊檔案或存取播放程式的屬性），物件仍然很有用。</span><span class="sxs-lookup"><span data-stu-id="fcbc0-122">However, the object is still useful for tasks that don't require the user interface, such as working with the library, playing digital audio files, or accessing properties of the Player.</span></span>

<span data-ttu-id="fcbc0-123">下列範例程式碼顯示一個簡單的主控台程式，它會在訊息方塊中顯示 Windows Media Player 的版本。</span><span class="sxs-lookup"><span data-stu-id="fcbc0-123">The following example code shows a simple console program that displays the Windows Media Player version in a message box.</span></span> <span data-ttu-id="fcbc0-124">範例程式碼會使用 ATL 來利用智慧型指標和 **CComBSTR** 字串類別。</span><span class="sxs-lookup"><span data-stu-id="fcbc0-124">The example code uses ATL to take advantage of smart pointers and the **CComBSTR** string class.</span></span>


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="fcbc0-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcbc0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcbc0-126">**在 c + + 程式中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="fcbc0-126">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




