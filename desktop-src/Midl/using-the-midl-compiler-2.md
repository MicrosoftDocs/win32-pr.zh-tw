---
title: 使用 MIDL 編譯器
description: MIDL 編譯器會自動安裝為平臺軟體發展工具組 (SDK) 安裝程式的一部分。
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Microsoft 介面定義語言 MIDL，工作
- MIDL 編譯器 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375213"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="2bf5a-105">使用 MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="2bf5a-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="2bf5a-106">MIDL 編譯器會自動安裝為平臺軟體發展工具組 (SDK) 安裝程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="2bf5a-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="2bf5a-107">下列主題描述 MIDL C 編譯器和 C 預處理器需求、遠端程序呼叫中的程式庫 (RPC) 產品，以及 MIDL 針對 DCOM 介面、RPC 介面和 OLE Automation 類型程式庫介面產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="2bf5a-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="2bf5a-108">叫用 MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="2bf5a-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="2bf5a-109">回應檔</span><span class="sxs-lookup"><span data-stu-id="2bf5a-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="2bf5a-110">C-MIDL 的預處理器需求</span><span class="sxs-lookup"><span data-stu-id="2bf5a-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="2bf5a-111">C/c + +-編譯器考慮</span><span class="sxs-lookup"><span data-stu-id="2bf5a-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="2bf5a-112">使用 \_ \_ Midl 預先定義的常數</span><span class="sxs-lookup"><span data-stu-id="2bf5a-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="2bf5a-113">MIDL 和 RPC</span><span class="sxs-lookup"><span data-stu-id="2bf5a-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="2bf5a-114">MIDL 和 COM</span><span class="sxs-lookup"><span data-stu-id="2bf5a-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="2bf5a-115">MIDL 和 ODL</span><span class="sxs-lookup"><span data-stu-id="2bf5a-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="2bf5a-116">如需有關組成 RPC 產品之檔案的詳細資訊，請參閱 [安裝 rpc 程式設計環境](/windows/desktop/Rpc/installing-the-rpc-programming-environment)。</span><span class="sxs-lookup"><span data-stu-id="2bf5a-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 