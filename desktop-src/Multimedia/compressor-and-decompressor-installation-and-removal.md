---
title: 壓縮和解壓縮安裝和移除
description: 壓縮和解壓縮安裝和移除
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，安裝壓縮機
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，安裝壓縮機
- ICInstall 函式
- ICRemove 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314707"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a><span data-ttu-id="3b246-107">壓縮和解壓縮安裝和移除</span><span class="sxs-lookup"><span data-stu-id="3b246-107">Compressor and Decompressor Installation and Removal</span></span>

<span data-ttu-id="3b246-108">應用程式可以使用已安裝在執行 Microsoft Windows 作業系統之系統上的壓縮機和 decompressors。</span><span class="sxs-lookup"><span data-stu-id="3b246-108">An application can use compressors and decompressors that are already installed on a system running the Microsoft Windows operating system.</span></span> <span data-ttu-id="3b246-109">應用程式也可以安裝壓縮機和 decompressors，以進行一般或特殊用途。</span><span class="sxs-lookup"><span data-stu-id="3b246-109">An application can also install compressors and decompressors for general or special uses.</span></span> <span data-ttu-id="3b246-110">大部分的應用程式都不需要安裝或移除壓縮機或 decompressors，因為這些應用程式通常是由安裝程式所安裝。</span><span class="sxs-lookup"><span data-stu-id="3b246-110">Most applications will not need to install or remove compressors or decompressors because they are usually installed by a setup program.</span></span> <span data-ttu-id="3b246-111">但是，應用程式可能會直接安裝壓縮程式，或將函數安裝為壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-111">An application might, however, install a compressor directly or install a function as a compressor.</span></span>

<span data-ttu-id="3b246-112">應用程式可以使用 [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) 函式，來安裝壓縮程式或解壓縮程式 (或作為壓縮程式或解壓縮程式) 的函式。</span><span class="sxs-lookup"><span data-stu-id="3b246-112">An application can install a compressor or decompressor (or a function used as a compressor or decompressor) by using the [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) function.</span></span> <span data-ttu-id="3b246-113">此函式會在登錄中建立專案，以識別壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-113">This function creates an entry in the registry identifying the compressor or decompressor.</span></span> <span data-ttu-id="3b246-114">您的應用程式或其他應用程式可以搜尋登錄，以判斷系統是否包含適用于其資料的壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-114">Your application or another application can search the registry to determine if the system contains a compressor or decompressor suitable for its data.</span></span> <span data-ttu-id="3b246-115">使用 **ICInstall** 安裝所有壓縮和解壓縮驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-115">Use **ICInstall** to install all compression and decompression drivers.</span></span>

<span data-ttu-id="3b246-116">應用程式可以使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 和 [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) 函式，找出並開啟已安裝的壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-116">An application can locate and open an installed compressor or decompressor by using the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="3b246-117">當應用程式使用壓縮程式或解壓縮程式完成時，它會使用 [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) 函數來關閉它。</span><span class="sxs-lookup"><span data-stu-id="3b246-117">When an application finishes using a compressor or decompressor, it closes it by using the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function.</span></span>

<span data-ttu-id="3b246-118">應用程式可以使用 [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) 函數，移除已安裝之壓縮程式或解壓縮程式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="3b246-118">An application can remove the registry entry for an installed compressor or decompressor by using the [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) function.</span></span> <span data-ttu-id="3b246-119">此函式會移除目前未載入記憶體中的壓縮程式或解壓縮程式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="3b246-119">This function removes the registry entry of a compressor or decompressor that is not currently loaded in memory.</span></span>

<span data-ttu-id="3b246-120">應用程式可以藉由安裝、開啟、關閉和移除，來限制使用壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="3b246-120">An application can restrict the use of a compressor or decompressor by installing, opening, closing, and removing it.</span></span>

<span data-ttu-id="3b246-121">或者，若要在內部使用函式做為壓縮程式或解壓縮程式，而不將它安裝在登錄中，應用程式可以使用 [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) 函數。</span><span class="sxs-lookup"><span data-stu-id="3b246-121">Alternatively, to use a function internally as a compressor or decompressor without installing it in the registry, an application can use the [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) function.</span></span> <span data-ttu-id="3b246-122">此函式需要呼叫的應用程式具有要當做壓縮程式或解壓縮程式使用之函式的位址。</span><span class="sxs-lookup"><span data-stu-id="3b246-122">This function requires the calling application to have the address of the function to be used as a compressor or decompressor.</span></span> <span data-ttu-id="3b246-123">當應用程式使用函式完成時，它必須使用 **ICClose** 來關閉它。</span><span class="sxs-lookup"><span data-stu-id="3b246-123">When the application finishes using the function, it must close it by using **ICClose**.</span></span> <span data-ttu-id="3b246-124">由於未安裝此函式，因此應用程式不需要從登錄中移除該函式。</span><span class="sxs-lookup"><span data-stu-id="3b246-124">Because the function was not installed, the application does not need to remove the function from the registry.</span></span>

<span data-ttu-id="3b246-125">當做壓縮程式或解壓縮程式使用之函式的內部結構，應該與可安裝的驅動程式所使用的 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 進入點函數相同。</span><span class="sxs-lookup"><span data-stu-id="3b246-125">The internal structure of a function used as a compressor or decompressor should be the same as the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) entry-point function used by installable drivers.</span></span> <span data-ttu-id="3b246-126">如需有關 **DriverProc** 進入點函數的詳細資訊，請參閱可 [安裝的驅動程式](installable-drivers.md)。</span><span class="sxs-lookup"><span data-stu-id="3b246-126">For more information about the **DriverProc** entry-point function, see [Installable Drivers](installable-drivers.md).</span></span>

> [!Note]  
> <span data-ttu-id="3b246-127">將函式安裝為壓縮程式或解壓縮程式的應用程式，必須在應用程式關閉之前移除該函式，讓其他應用程式不會嘗試使用該函數。</span><span class="sxs-lookup"><span data-stu-id="3b246-127">An application installing a function as a compressor or decompressor must remove the function before the application is closed so other applications do not try to use the function.</span></span> <span data-ttu-id="3b246-128">移除函式時，應用程式必須使用用來安裝它的四個字元碼來識別它。</span><span class="sxs-lookup"><span data-stu-id="3b246-128">When removing a function, the application must identify it with the four-character code used to install it.</span></span>

 

 

 