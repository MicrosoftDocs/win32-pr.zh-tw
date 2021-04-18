---
description: 全螢幕 Direct3D 應用程式會提供 windows 控制碼給 Direct3D 執行時間。
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: " (Direct3D 9) 的多執行緒問題"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385607"
---
# <a name="multithreading-issues-direct3d-9"></a><span data-ttu-id="236e1-103"> (Direct3D 9) 的多執行緒問題</span><span class="sxs-lookup"><span data-stu-id="236e1-103">Multithreading Issues (Direct3D 9)</span></span>

<span data-ttu-id="236e1-104">全螢幕 Direct3D 應用程式會提供 windows 控制碼給 Direct3D 執行時間。</span><span class="sxs-lookup"><span data-stu-id="236e1-104">Full-screen Direct3D applications provide a window handle to the Direct3D run time.</span></span> <span data-ttu-id="236e1-105">視窗會與執行時間連結。</span><span class="sxs-lookup"><span data-stu-id="236e1-105">The window is hooked by the run time.</span></span> <span data-ttu-id="236e1-106">這表示，所有傳遞至應用程式視窗訊息程式的訊息，都是由 Direct3D 執行時間本身的訊息處理常式所檢查。</span><span class="sxs-lookup"><span data-stu-id="236e1-106">This means that all messages passed to the application's window message procedure have first been examined by the Direct3D run time's own message-handling procedure.</span></span>

<span data-ttu-id="236e1-107">顯示模式變更會受到基礎作業系統內建的支援常式影響。</span><span class="sxs-lookup"><span data-stu-id="236e1-107">Display mode changes are affected by support routines built into the underlying operating system.</span></span> <span data-ttu-id="236e1-108">發生模式變更時，系統會將數個訊息廣播至所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="236e1-108">When mode changes occur, the system broadcasts several messages to all applications.</span></span> <span data-ttu-id="236e1-109">在 Direct3D 應用程式中，訊息會在視窗程式執行緒上收到，這不一定是呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 或 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) (的相同執行緒，也不一定是 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)的最終發行版本，而這可能會導致顯示模式變更) 。</span><span class="sxs-lookup"><span data-stu-id="236e1-109">In Direct3D applications, the messages are received on the window procedure thread, which is not necessarily the same thread that called [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) or [**IDirect3D9::CreateDevice**](/windows/desktop/api) (or the final Release of [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), which can cause a display mode change).</span></span> <span data-ttu-id="236e1-110">Direct3D 執行時間會在內部維護數個重要區段。</span><span class="sxs-lookup"><span data-stu-id="236e1-110">The Direct3D run time maintains several critical sections internally.</span></span> <span data-ttu-id="236e1-111">因為 **IDirect3DDevice9：： Reset** 或 **IDirect3D9：： CreateDevice** 所造成的模式切換中至少會保留其中一個重要區段，所以當應用程式收到模式變更相關的視窗訊息時，仍會保留這些重要區段。</span><span class="sxs-lookup"><span data-stu-id="236e1-111">Because at least one of these critical sections is held across the mode switch caused by **IDirect3DDevice9::Reset** or **IDirect3D9::CreateDevice**, these critical sections are still held when the application receives the mode-change related window messages.</span></span>

<span data-ttu-id="236e1-112">這種設計對多執行緒應用程式有一些影響。</span><span class="sxs-lookup"><span data-stu-id="236e1-112">This design has some implications for multithreaded applications.</span></span> <span data-ttu-id="236e1-113">尤其是，應用程式必須務必將其視窗訊息處理執行緒從其 Direct3D 執行緒中緊密隔離。</span><span class="sxs-lookup"><span data-stu-id="236e1-113">In particular, an application must be sure to strongly segregate its window message handling threads from its Direct3D threads.</span></span> <span data-ttu-id="236e1-114">在某個執行緒上造成模式變更的應用程式，但在其視窗程式中的不同執行緒上進行 Direct3D 呼叫，會有鎖死的風險。</span><span class="sxs-lookup"><span data-stu-id="236e1-114">An application that causes a mode change on one thread but makes Direct3D calls on a different thread in its window procedure is in danger of deadlock.</span></span>

<span data-ttu-id="236e1-115">基於這些理由，Direct3D 的設計目的是要讓 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)、 [**IDirect3D9：： CreateDevice**](/windows/desktop/api)、 [**IDirect3DDevice9：： TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)或最終發行的 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 只能從處理視窗訊息的相同執行緒呼叫。</span><span class="sxs-lookup"><span data-stu-id="236e1-115">For these reasons, Direct3D is designed so that the methods [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9::CreateDevice**](/windows/desktop/api), [**IDirect3DDevice9::TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel), or the final Release of [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) can only be called from the same thread that handles window messages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="236e1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="236e1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="236e1-117">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="236e1-117">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
