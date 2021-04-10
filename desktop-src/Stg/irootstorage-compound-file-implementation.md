---
title: IRootStorage-複合檔案執行
description: IRootStorage 的 COM 複合檔案執行，可讓您支援在低記憶體或磁碟空間不足的情況下儲存檔案。 如需此介面行為方式的詳細資訊，請參閱 IRootStorage。
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675912"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="86fd4-105">IRootStorage-複合檔案執行</span><span class="sxs-lookup"><span data-stu-id="86fd4-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="86fd4-106">[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)的 COM 複合檔案執行，可讓您支援在低記憶體或磁碟空間不足的情況下儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="86fd4-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="86fd4-107">如需此介面行為方式的詳細資訊，請參閱 **IRootStorage**。</span><span class="sxs-lookup"><span data-stu-id="86fd4-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="86fd4-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="86fd4-108">When to Use</span></span>

<span data-ttu-id="86fd4-109">僅使用系統提供的 [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) 執行，以支援在低記憶體的情況下儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="86fd4-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fd4-110">備註</span><span class="sxs-lookup"><span data-stu-id="86fd4-110">Remarks</span></span>

<span data-ttu-id="86fd4-111">您可以呼叫 COM 的 [**IRootStorage：： SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) 實作為另一個檔案的一般另存新檔作業。</span><span class="sxs-lookup"><span data-stu-id="86fd4-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="86fd4-112">不過，這樣做的應用程式可能與未來的 COM 儲存體層代不相容。</span><span class="sxs-lookup"><span data-stu-id="86fd4-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="86fd4-113">為了避免這種可能性，執行另存新檔作業的應用程式應該手動建立第二個複合檔案，並叫用 [**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)。</span><span class="sxs-lookup"><span data-stu-id="86fd4-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="86fd4-114">**IRootStorage：： SwitchToFile** 方法只能在緊急 (的低記憶體或磁碟空間) 情況下使用。</span><span class="sxs-lookup"><span data-stu-id="86fd4-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86fd4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="86fd4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86fd4-116">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="86fd4-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="86fd4-117">**IRootStorage::SwitchToFile**</span><span class="sxs-lookup"><span data-stu-id="86fd4-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




