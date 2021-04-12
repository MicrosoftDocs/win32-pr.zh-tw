---
title: 使用 System-Supplied 代理
description: 使用 System-Supplied 代理
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311390"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="4b29e-103">使用 System-Supplied 代理</span><span class="sxs-lookup"><span data-stu-id="4b29e-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="4b29e-104">若要針對您的 DLL 伺服器使用系統提供的代理程式，請在登錄中註冊指定空字串或 **Null** 的 dll 以做為 [DllSurrogate](dllsurrogate.md) 值。</span><span class="sxs-lookup"><span data-stu-id="4b29e-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="4b29e-105">當 DLL 伺服器的啟用要求是針對 COM 而指定時，COM 會啟動預設的代理程式和要求的 DLL (方法是在內部) 的啟動命令列上指定 CLSID，以避免個別的呼叫。</span><span class="sxs-lookup"><span data-stu-id="4b29e-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="4b29e-106"> (需在代理程式中執行多部 DLL 伺服器的詳細資訊，請參閱 [代理共用](surrogate-sharing.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="4b29e-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="4b29e-107">代理進程的預設實作為混合執行緒模型樣式的虛擬 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4b29e-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="4b29e-108">當多個 DLL 伺服器載入至單一代理程式時，此程式會使用該伺服器的登錄中指定的執行緒模型，確保每個 DLL 伺服器都具現化。</span><span class="sxs-lookup"><span data-stu-id="4b29e-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="4b29e-109">所有載入的自由執行緒伺服器都會在多執行緒單元中一起運作，而每個單元執行緒伺服器則會位於單一執行緒的單元中。</span><span class="sxs-lookup"><span data-stu-id="4b29e-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="4b29e-110">如果 DLL 伺服器同時支援這兩種執行緒模型，COM 將會選擇多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="4b29e-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="4b29e-111">寫入這個代理程式是為了讓 COM 處理卸載 DLL 伺服器和終止代理進程的作業。</span><span class="sxs-lookup"><span data-stu-id="4b29e-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="4b29e-112">系統提供的代理將非常適合大部分的開發人員，而且很容易使用。</span><span class="sxs-lookup"><span data-stu-id="4b29e-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="4b29e-113">不過，具有特殊考慮的開發人員可能會決定需要自訂的代理。</span><span class="sxs-lookup"><span data-stu-id="4b29e-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="4b29e-114">如需詳細資訊，請參閱 [撰寫自訂代理](writing-a-custom-surrogate.md)。</span><span class="sxs-lookup"><span data-stu-id="4b29e-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b29e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b29e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b29e-116">DLL 代理</span><span class="sxs-lookup"><span data-stu-id="4b29e-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




