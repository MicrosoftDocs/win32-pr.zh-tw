---
title: 介面封送處理
description: 介面封送處理
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106999805"
---
# <a name="interface-marshaling"></a><span data-ttu-id="31983-103">介面封送處理</span><span class="sxs-lookup"><span data-stu-id="31983-103">Interface Marshaling</span></span>

<span data-ttu-id="31983-104">除非您知道您的介面永遠不會跨整個單元、執行緒或進程界限使用，否則您必須決定如何為您的介面提供封送處理支援。</span><span class="sxs-lookup"><span data-stu-id="31983-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="31983-105">有三種方式可以提供封送處理支援：</span><span class="sxs-lookup"><span data-stu-id="31983-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="31983-106">撰寫您自己的 proxy/stub 程式碼，以呼叫 COM 通道，進而呼叫 RPC 執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="31983-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="31983-107">理論上，您可以這麼做，但在實務上，幾乎不可能進行大量的工作。</span><span class="sxs-lookup"><span data-stu-id="31983-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="31983-108">描述介面定義語言中的介面 (IDL) 檔，並使用 MIDL 編譯器來產生 proxy/stub DLL。</span><span class="sxs-lookup"><span data-stu-id="31983-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="31983-109">這個方法會以可接受的資料類型，提供最佳效能和最大的彈性。</span><span class="sxs-lookup"><span data-stu-id="31983-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="31983-110">使用 MIDL 產生的 proxy 存根，您不僅可以控制記憶體管理，也可以控制跨不同平臺的複雜資料類型封送處理和封送處理。</span><span class="sxs-lookup"><span data-stu-id="31983-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="31983-111">使用 MIDL 來產生系統在執行時間用來提供封送處理支援的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="31983-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="31983-112">這是執行封送處理支援的最簡單方式。</span><span class="sxs-lookup"><span data-stu-id="31983-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="31983-113">您只需要產生類型程式庫並加以註冊。</span><span class="sxs-lookup"><span data-stu-id="31983-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="31983-114">您的介面必須是 [**oleautomation**](/windows/desktop/Midl/oleautomation) 或 [**雙重**](/windows/desktop/Midl/dual)) 的自動化相容 (，這會對您可以用來做為方法參數的資料類型類型有一些限制。</span><span class="sxs-lookup"><span data-stu-id="31983-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="31983-115">不過，在大部分情況下，讓您的介面可供以其他語言（例如 Microsoft Visual Basic 和 JAVA）撰寫的程式存取，比資料類型的限制還高。</span><span class="sxs-lookup"><span data-stu-id="31983-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31983-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="31983-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31983-117">物件間通訊</span><span class="sxs-lookup"><span data-stu-id="31983-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 