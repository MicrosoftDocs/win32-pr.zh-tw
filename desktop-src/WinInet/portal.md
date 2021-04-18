---
title: Windows 網際網路
description: Microsoft Windows Internet (WinINet) 應用程式開發介面 (API) 可讓應用程式存取標準網際網路通訊協定，例如 FTP 和 HTTP。 為了方便使用，WinINet 將這些通訊協定抽象化為高階介面。
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows 網際網路 WinINet
- WinINet WinINet，入口網站
- Windows 網際網路 WinINet、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463512"
---
# <a name="windows-internet"></a><span data-ttu-id="01e83-107">Windows 網際網路</span><span class="sxs-lookup"><span data-stu-id="01e83-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="01e83-108">目的</span><span class="sxs-lookup"><span data-stu-id="01e83-108">Purpose</span></span>

<span data-ttu-id="01e83-109">Microsoft Windows Internet (WinINet) 應用程式開發介面 (API) 可讓應用程式存取標準網際網路通訊協定，例如 FTP 和 HTTP。</span><span class="sxs-lookup"><span data-stu-id="01e83-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="01e83-110">為了方便使用，WinINet 將這些通訊協定抽象化為高階介面。</span><span class="sxs-lookup"><span data-stu-id="01e83-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="01e83-111">適用時</span><span class="sxs-lookup"><span data-stu-id="01e83-111">Where applicable</span></span>

<span data-ttu-id="01e83-112">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="01e83-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="01e83-113">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="01e83-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="01e83-114">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="01e83-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="01e83-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="01e83-115">Developer audience</span></span>

<span data-ttu-id="01e83-116">WinINet 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="01e83-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="01e83-117">它需要對 FTP 和 HTTP 通訊協定有基本的瞭解。</span><span class="sxs-lookup"><span data-stu-id="01e83-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="01e83-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="01e83-118">Run-time requirements</span></span>

<span data-ttu-id="01e83-119">使用 WinINet API 的應用程式需要 Windows NT 4.0 或更新版本，或 Windows Me/98/95。</span><span class="sxs-lookup"><span data-stu-id="01e83-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="01e83-120">如需有關使用特定程式設計專案所需之作業系統或元件的詳細資訊，請參閱檔的需求一節。</span><span class="sxs-lookup"><span data-stu-id="01e83-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01e83-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="01e83-121">In this section</span></span>



| <span data-ttu-id="01e83-122">主題</span><span class="sxs-lookup"><span data-stu-id="01e83-122">Topic</span></span>                                                          | <span data-ttu-id="01e83-123">描述</span><span class="sxs-lookup"><span data-stu-id="01e83-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="01e83-124">關於 Windows 網際網路</span><span class="sxs-lookup"><span data-stu-id="01e83-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="01e83-125">Windows 網際網路 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="01e83-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="01e83-126">使用 Windows 網際網路</span><span class="sxs-lookup"><span data-stu-id="01e83-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="01e83-127">Windows 網際網路 API 的程式設計指南。</span><span class="sxs-lookup"><span data-stu-id="01e83-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="01e83-128">Windows 網際網路參考</span><span class="sxs-lookup"><span data-stu-id="01e83-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="01e83-129">Windows 網際網路 API 的參考檔。</span><span class="sxs-lookup"><span data-stu-id="01e83-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="01e83-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="01e83-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e83-131">Microsoft Windows HTTP Services (WinHTTP) </span><span class="sxs-lookup"><span data-stu-id="01e83-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

