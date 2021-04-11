---
title: Microsoft 介面定義語言
description: Microsoft 介面定義語言 (MIDL) 定義用戶端與伺服器程式之間的介面。
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- 'MIDL MIDL， (查看 Microsoft 介面定義語言 MIDL ) '
- Microsoft 介面定義語言 MIDL
- Microsoft 介面定義語言 MIDL、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023373"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="030fc-107">Microsoft 介面定義語言</span><span class="sxs-lookup"><span data-stu-id="030fc-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="030fc-108">目的</span><span class="sxs-lookup"><span data-stu-id="030fc-108">Purpose</span></span>

<span data-ttu-id="030fc-109">Microsoft 介面定義語言 (MIDL) 定義用戶端與伺服器程式之間的介面。</span><span class="sxs-lookup"><span data-stu-id="030fc-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="030fc-110">Microsoft 在平臺軟體發展工具組中包含 MIDL 編譯器 (SDK) ，可讓開發人員建立介面定義語言 (IDL) 檔案和應用程式佈建檔 () RPC (介面和 COM/DCOM 介面進行遠端程序呼叫所需的) ACF。</span><span class="sxs-lookup"><span data-stu-id="030fc-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="030fc-111">MIDL 也支援產生 OLE Automation 的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="030fc-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="030fc-112">適用時</span><span class="sxs-lookup"><span data-stu-id="030fc-112">Where applicable</span></span>

<span data-ttu-id="030fc-113">MIDL 可以在所有以 Windows 作業系統為基礎的用戶端/伺服器應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="030fc-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="030fc-114">它也可以用來建立適用于異類網路環境的用戶端和伺服器程式，這些環境包含 Unix 和 Apple 等作業系統。</span><span class="sxs-lookup"><span data-stu-id="030fc-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="030fc-115">Microsoft 支援開放式群組 (先前稱為開放式 Software Foundation) DCE 標準的 RPC 互通性。</span><span class="sxs-lookup"><span data-stu-id="030fc-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="030fc-116">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="030fc-116">Developer audience</span></span>

<span data-ttu-id="030fc-117">使用 MIDL 與 RPC 時，熟悉 C/c + + 程式設計，而且必須使用 RPC 架構。</span><span class="sxs-lookup"><span data-stu-id="030fc-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="030fc-118">當使用 MIDL 與 COM 時，必須熟悉 c + + 程式設計，以及將它套用至 COM 的 RPC 架構，或者也需要熟悉 OLE Automation 模型腳本和型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="030fc-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="030fc-119">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="030fc-119">Run-time requirements</span></span>

<span data-ttu-id="030fc-120">使用 MIDL 的適當執行時間程式庫包含在 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="030fc-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="030fc-121">當您安裝 Windows SDK 時，會安裝 MIDL 編譯器和 RPC 開發環境的元件。</span><span class="sxs-lookup"><span data-stu-id="030fc-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="030fc-122">如需詳細資訊，請參閱 [使用 MIDL 編譯器](using-the-midl-compiler-2.md) 和 [安裝 RPC 程式設計環境](/windows/desktop/Rpc/installing-the-rpc-programming-environment)。</span><span class="sxs-lookup"><span data-stu-id="030fc-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="030fc-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="030fc-123">In this section</span></span>



| <span data-ttu-id="030fc-124">主題</span><span class="sxs-lookup"><span data-stu-id="030fc-124">Topic</span></span>                                                                                               | <span data-ttu-id="030fc-125">描述</span><span class="sxs-lookup"><span data-stu-id="030fc-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="030fc-126">概觀</span><span class="sxs-lookup"><span data-stu-id="030fc-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="030fc-127">MIDL 和 MIDL 編譯器的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="030fc-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="030fc-128">使用 MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="030fc-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="030fc-129">使用 MIDL compilter 來產生 RPC 存根的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="030fc-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="030fc-130">介面定義和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="030fc-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="030fc-131">RPC 特定介面定義和類型程式庫的檔。</span><span class="sxs-lookup"><span data-stu-id="030fc-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="030fc-132">MIDL Command-Line 參考</span><span class="sxs-lookup"><span data-stu-id="030fc-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="030fc-133">MIDL 編譯器命令列參數的檔。</span><span class="sxs-lookup"><span data-stu-id="030fc-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="030fc-134">MIDL 語言參考</span><span class="sxs-lookup"><span data-stu-id="030fc-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="030fc-135">MIDL 編譯器語言參考。</span><span class="sxs-lookup"><span data-stu-id="030fc-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="030fc-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="030fc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030fc-137"> (RPC) 的遠端程序呼叫 </span><span class="sxs-lookup"><span data-stu-id="030fc-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

