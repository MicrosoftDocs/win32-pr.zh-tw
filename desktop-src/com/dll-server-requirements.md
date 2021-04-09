---
title: DLL 伺服器需求
description: 雖然大部分的 Dll 都可以在代理中執行，但是某些 Dll 無法執行。
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022102"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="43d80-103">DLL 伺服器需求</span><span class="sxs-lookup"><span data-stu-id="43d80-103">DLL Server Requirements</span></span>

<span data-ttu-id="43d80-104">雖然大部分的 Dll 都可以在代理中執行，但是某些 Dll 無法執行。</span><span class="sxs-lookup"><span data-stu-id="43d80-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="43d80-105">如果您想要使用系統提供的代理，DLL 必須有良好的行為。</span><span class="sxs-lookup"><span data-stu-id="43d80-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="43d80-106">例如，呼叫從用戶端註冊回呼之方法的 DLL，會嘗試叫用這些回呼，如同它所接收的函式指標是否為其位址空間中的指示（不是如此）。</span><span class="sxs-lookup"><span data-stu-id="43d80-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="43d80-107">同樣地，使用預期用戶端存取之全域變數的 DLL 無法運作。</span><span class="sxs-lookup"><span data-stu-id="43d80-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="43d80-108">一般情況下，無法正確封送處理的參數將會使 DLL 伺服器無法在用戶端進程之外執行。</span><span class="sxs-lookup"><span data-stu-id="43d80-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="43d80-109">在許多情況下，您可以撰寫明確設計來彌補「不良」行為的自訂代理。</span><span class="sxs-lookup"><span data-stu-id="43d80-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="43d80-110"> (需詳細資訊，請參閱 [撰寫自訂代理](writing-a-custom-surrogate.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="43d80-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="43d80-111">如果 DLL 伺服器使用自訂介面，您必須確定這些介面可使用封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="43d80-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="43d80-112">例如，您可以建立並註冊 proxy DLL，或是提供並註冊類型程式庫，讓伺服器能夠在代理程式中執行時正常運作。</span><span class="sxs-lookup"><span data-stu-id="43d80-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="43d80-113">DLL 伺服器只會載入至在適當的安全性內容中執行的代理程式。</span><span class="sxs-lookup"><span data-stu-id="43d80-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="43d80-114">DLL 伺服器代理的安全性內容是以與 EXE 伺服器相同的方式來決定。</span><span class="sxs-lookup"><span data-stu-id="43d80-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="43d80-115">除非在伺服器的 [AppID](appid-clsid.md)登錄區段中設定了 **RunAs** 值（決定安全性內容），否則 DLL 伺服器代理會在與用戶端相同的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="43d80-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43d80-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="43d80-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43d80-117">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="43d80-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




