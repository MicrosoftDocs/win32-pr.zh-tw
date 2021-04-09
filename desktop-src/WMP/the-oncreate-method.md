---
title: '>oncreate 方法'
description: '>oncreate 方法'
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player 外掛程式，>oncreate 方法
- 外掛程式，>oncreate 方法
- 使用者介面外掛程式，>oncreate 方法
- UI 外掛程式，>oncreate 方法
- '>oncreate 方法'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839395"
---
# <a name="the-oncreate-method"></a><span data-ttu-id="88549-108">>oncreate 方法</span><span class="sxs-lookup"><span data-stu-id="88549-108">The OnCreate Method</span></span>

<span data-ttu-id="88549-109">第一次建立外掛程式視窗時，會呼叫 >oncreate 方法。</span><span class="sxs-lookup"><span data-stu-id="88549-109">The OnCreate method is called when the plug-in window is first created.</span></span>

<span data-ttu-id="88549-110">下列程式碼會用來執行此方法：</span><span class="sxs-lookup"><span data-stu-id="88549-110">The following code is used to implement this method:</span></span>


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



<span data-ttu-id="88549-111">這個方法會建立 **搜尋** 按鈕，並將其與在檔案 \_ 開頭定義的 IDC 搜尋命令識別碼產生關聯：</span><span class="sxs-lookup"><span data-stu-id="88549-111">This method creates the **Search** button and associates it with the IDC\_SEARCH command ID, which is defined at the beginning of the file:</span></span>


```C++
#define IDC_SEARCH 2000

```



<span data-ttu-id="88549-112">此命令識別碼會對應至先前所述之訊息對應區段中的 OnSearch 方法。</span><span class="sxs-lookup"><span data-stu-id="88549-112">This command ID is mapped to the OnSearch method in the message map section described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88549-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="88549-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88549-114">**執行 CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="88549-114">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




