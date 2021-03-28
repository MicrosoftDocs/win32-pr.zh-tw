---
title: Direct3D 版本之間的執行緒差異
description: 許多多執行緒程式設計模型會使用同步處理原始物件 (例如 mutex) 來建立重要區段，並防止一次有多個執行緒存取程式碼。
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375972"
---
# <a name="threading-differences-between-direct3d-versions"></a><span data-ttu-id="484e8-103">Direct3D 版本之間的執行緒差異</span><span class="sxs-lookup"><span data-stu-id="484e8-103">Threading Differences between Direct3D Versions</span></span>

<span data-ttu-id="484e8-104">許多多執行緒程式設計模型會使用同步處理原始物件 (例如 mutex) 來建立重要區段，並防止一次有多個執行緒存取程式碼。</span><span class="sxs-lookup"><span data-stu-id="484e8-104">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span>

<span data-ttu-id="484e8-105">不過， [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面的資源建立方法是設計成可重複進行，而不需要同步處理原始物件和重要區段。</span><span class="sxs-lookup"><span data-stu-id="484e8-105">However, the resource creation methods of the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface were designed to be re-entrant, without requiring synchronization primitives and critical sections.</span></span> <span data-ttu-id="484e8-106">因此，資源建立方法既有效率又容易使用。</span><span class="sxs-lookup"><span data-stu-id="484e8-106">As a result, the resource creation methods are efficient and easy to use.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="484e8-107">Direct3D 11、10和9之間的差異：</span><span class="sxs-lookup"><span data-stu-id="484e8-107">Differences between Direct3D 11, 10 and 9:</span></span><br/> <span data-ttu-id="484e8-108">Direct3D 11 的預設值大多為安全線程，並且會繼續允許應用程式使用 D3D11 \_ CREATE DEVICE SINGLETHREADED 來退出 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="484e8-108">Direct3D 11 defaults to mostly thread-safe and continues to allow applications to opt-out using D3D11\_CREATE\_DEVICE\_SINGLETHREADED.</span></span> <span data-ttu-id="484e8-109">如果應用程式選擇不是安全線程，則必須遵守執行緒規則。</span><span class="sxs-lookup"><span data-stu-id="484e8-109">If applications opt-out of being thread-safe, they must adhere to threading rules.</span></span> <span data-ttu-id="484e8-110">執行時間會代表允許平行線程執行的應用程式來同步處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="484e8-110">The runtime synchronizes threads on behalf of the application allowing concurrent threads to run.</span></span> <span data-ttu-id="484e8-111">事實上，Direct3D 11 中的同步處理比使用 Direct3D 10 中的安全線程層更有效率。</span><span class="sxs-lookup"><span data-stu-id="484e8-111">In fact, the synchronization in Direct3D 11 is more efficient than using the thread-safe layer in Direct3D 10.</span></span><br/> <span data-ttu-id="484e8-112">Direct3D 10 一次只能支援一個執行緒執行。</span><span class="sxs-lookup"><span data-stu-id="484e8-112">Direct3D 10 can support the execution of only one thread at a time.</span></span> <span data-ttu-id="484e8-113">Direct3D 10 是完全安全線程，可讓應用程式使用 D3D10 \_ 建立 \_ 裝置 \_ 單一執行緒來退出該行為 \_ 。</span><span class="sxs-lookup"><span data-stu-id="484e8-113">Direct3D 10 is fully thread safe and allows an application to opt-out of that behavior by using D3D10\_CREATE\_DEVICE\_SINGLE\_THREADED.</span></span> <br/> <span data-ttu-id="484e8-114">Direct3D 9 不會預設為安全線程。</span><span class="sxs-lookup"><span data-stu-id="484e8-114">Direct3D 9 does not default to thread safe.</span></span> <span data-ttu-id="484e8-115">不過，當您呼叫 [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) 或 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 來建立裝置時，您可以指定 D3DCREATE \_ 多執行緒旗標，讓 Direct3D 9 API 成為安全線程。</span><span class="sxs-lookup"><span data-stu-id="484e8-115">However, when you call [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) or [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) to create a device, you can specify the D3DCREATE\_MULTITHREADED flag to make the Direct3D 9 API thread safe.</span></span> <span data-ttu-id="484e8-116">這會導致大量的同步處理額外負荷。</span><span class="sxs-lookup"><span data-stu-id="484e8-116">This causes significant synchronization overhead.</span></span> <span data-ttu-id="484e8-117">因此，不建議將 Direct3D 9 API 執行緒設為安全，因為效能可能會降低。</span><span class="sxs-lookup"><span data-stu-id="484e8-117">Therefore, making the Direct3D 9 API thread safe is not recommended because performance can be degraded.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="484e8-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="484e8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="484e8-119">多執行緒</span><span class="sxs-lookup"><span data-stu-id="484e8-119">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

