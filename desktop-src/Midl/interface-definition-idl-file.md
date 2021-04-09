---
title: " (IDL) 檔案的介面定義"
description: 依照慣例，包含介面和型別程式庫定義的檔案稱為 IDL 檔案，且副檔名為 .idl。
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- 介面 MIDL、IDL 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950daa2c1841f6e4b3f015f14e373804fcd34b80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681890"
---
# <a name="interface-definition-idl-file"></a><span data-ttu-id="bb8dd-104"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="bb8dd-104">Interface Definition (IDL) File</span></span>

<span data-ttu-id="bb8dd-105">依照慣例，包含介面和型別程式庫定義的檔案稱為 IDL 檔案，且副檔名為 .idl。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-105">By convention, the file that contains interface and type library definitions is called an IDL file, and has an .idl file name extension.</span></span> <span data-ttu-id="bb8dd-106">實際上，MIDL 編譯器會剖析介面定義檔，而不論它的副檔名為何。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-106">In reality, the MIDL compiler will parse an interface definition file regardless of its extension.</span></span> <span data-ttu-id="bb8dd-107">介面是由關鍵字 [**介面**](interface.md)所識別。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-107">An interface is identified by the keyword [**interface**](interface.md).</span></span>

<span data-ttu-id="bb8dd-108">每個介面都是由標頭和主體組成。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-108">Each interface consists of a header and a body.</span></span> <span data-ttu-id="bb8dd-109">介面標頭包含適用于整個介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-109">The interface header contains attributes that apply to the entire interface.</span></span> <span data-ttu-id="bb8dd-110">介面的主體包含其餘的介面定義。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-110">The body of the interface contains the remaining interface definitions.</span></span> <span data-ttu-id="bb8dd-111">如需介面和 IDL 檔案的總覽，請參閱 [介面定義語言 (IDL) ](/windows/desktop/Rpc/the-interface-definition-language-idl-file)檔。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-111">For an overview of interfaces and IDL files, see [The Interface Definition Language (IDL) File](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span></span> <span data-ttu-id="bb8dd-112">如需可在介面標頭中使用之屬性的摘要，請參閱 [IDL 屬性](idl-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="bb8dd-112">For a summary of attributes that can be used in an interface header, see [IDL Attributes](idl-attributes.md).</span></span>

 

 