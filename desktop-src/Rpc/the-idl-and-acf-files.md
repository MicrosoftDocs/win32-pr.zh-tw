---
title: IDL 和 ACF 檔案
description: Microsoft 介面定義語言 (MIDL) 的語法是以 C 程式設計語言的語法為基礎。 當這項 MIDL 描述中的語言概念未完整定義時，就會隱含該詞彙的 C 語言定義。
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- 遠端程序呼叫 RPC、描述、IDL 和 ACF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7f739e50fd4e04ae35a11adcbbc936cd3cb36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933438"
---
# <a name="the-idl-and-acf-files"></a><span data-ttu-id="014d8-105">IDL 和 ACF 檔案</span><span class="sxs-lookup"><span data-stu-id="014d8-105">The IDL and ACF Files</span></span>

<span data-ttu-id="014d8-106">Microsoft 介面定義語言 (MIDL) 的語法是以 C 程式設計語言的語法為基礎。</span><span class="sxs-lookup"><span data-stu-id="014d8-106">The syntax of the Microsoft Interface Definition Language (MIDL) is based on the syntax of the C programming language.</span></span> <span data-ttu-id="014d8-107">當這項 MIDL 描述中的語言概念未完整定義時，就會隱含該詞彙的 C 語言定義。</span><span class="sxs-lookup"><span data-stu-id="014d8-107">When a language concept in this description of MIDL is not fully defined, the C-language definition of that term is implied.</span></span>

<span data-ttu-id="014d8-108">MIDL 設計會指定兩個不同的檔案：介面定義語言 (IDL) 檔和應用程式佈建檔 (ACF) 。</span><span class="sxs-lookup"><span data-stu-id="014d8-108">The MIDL design specifies two distinct files: the Interface Definition Language (IDL) file and the application configuration file (ACF).</span></span> <span data-ttu-id="014d8-109">這些檔案包含的屬性，會將管理遠端程序呼叫的 C 語言存根檔案的產生導向 (RPC) 。</span><span class="sxs-lookup"><span data-stu-id="014d8-109">These files contain attributes that direct the generation of the C-language stub files that manage the remote procedure call (RPC).</span></span> <span data-ttu-id="014d8-110">IDL 檔案包含用戶端與伺服器程式之間的介面描述。</span><span class="sxs-lookup"><span data-stu-id="014d8-110">The IDL file contains a description of the interface between the client and the server programs.</span></span> <span data-ttu-id="014d8-111">RPC 應用程式會使用 ACF 檔來描述組成特定作業環境之硬體和作業系統的特定介面特性。</span><span class="sxs-lookup"><span data-stu-id="014d8-111">RPC applications use the ACF file to describe the characteristics of the interface that are specific to the hardware and operating system that make up a particular operating environment.</span></span> <span data-ttu-id="014d8-112">將此資訊分割成兩個檔案的目的，是要讓軟體介面與只影響操作環境的特性分開。</span><span class="sxs-lookup"><span data-stu-id="014d8-112">The purpose of dividing this information into two files is to keep the software interface separate from characteristics that affect only the operating environment.</span></span>

<span data-ttu-id="014d8-113">IDL 檔案會指定用戶端與伺服器之間的網路合約，也就是 IDL 檔案會指定在用戶端與伺服器之間傳輸的內容。</span><span class="sxs-lookup"><span data-stu-id="014d8-113">The IDL file specifies a network contract between the client and server—that is, the IDL file specifies what is transmitted between the client and the server.</span></span> <span data-ttu-id="014d8-114">將此資訊與作業環境相關的資訊保持不變，可將 IDL 檔案移植到其他環境。</span><span class="sxs-lookup"><span data-stu-id="014d8-114">Keeping this information distinct from the information about the operating environment makes the IDL file portable to other environments.</span></span> <span data-ttu-id="014d8-115">IDL 檔案是由兩個部分所組成： [介面標頭](the-idl-interface-header.md) 和 [介面主體](the-idl-interface-body.md)。</span><span class="sxs-lookup"><span data-stu-id="014d8-115">The IDL file consists of two parts: an [interface header](the-idl-interface-header.md) and an [interface body](the-idl-interface-body.md).</span></span>

<span data-ttu-id="014d8-116">ACF 所指定的屬性只會影響本機效能，而不會影響網路合約。</span><span class="sxs-lookup"><span data-stu-id="014d8-116">The ACF specifies attributes that affect only local performance rather than the network contract.</span></span> <span data-ttu-id="014d8-117">Microsoft RPC 允許您合併單一 IDL 檔案中的 ACF 和 IDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="014d8-117">Microsoft RPC allows you to combine the ACF and IDL attributes in a single IDL file.</span></span> <span data-ttu-id="014d8-118">您也可以在單一 IDL 檔案中結合多個介面 (及其 ACF) 。</span><span class="sxs-lookup"><span data-stu-id="014d8-118">You can also combine multiple interfaces in a single IDL file (and its ACF).</span></span>

<span data-ttu-id="014d8-119">本節摘要說明 IDL 和 ACF 檔案中所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="014d8-119">This section summarizes the attributes that are specified in the IDL and ACF files.</span></span> <span data-ttu-id="014d8-120">它的目的只是要提供總覽。</span><span class="sxs-lookup"><span data-stu-id="014d8-120">It is intended to only provide an overview.</span></span> <span data-ttu-id="014d8-121">如需詳細資訊，請參閱 [Midl 語言參考](/windows/desktop/Midl/midl-language-reference)，以及 [midl Command-Line 參考](/windows/desktop/Midl/midl-command-line-reference)。</span><span class="sxs-lookup"><span data-stu-id="014d8-121">For more detailed information, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference), and the [MIDL Command-Line Reference](/windows/desktop/Midl/midl-command-line-reference).</span></span> <span data-ttu-id="014d8-122">本章節中的討論內容將在下列主題中顯示：</span><span class="sxs-lookup"><span data-stu-id="014d8-122">The discussion in this section is presented in the following topics:</span></span>

-   [<span data-ttu-id="014d8-123">介面定義語言 (IDL) 檔</span><span class="sxs-lookup"><span data-stu-id="014d8-123">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
-   [<span data-ttu-id="014d8-124">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="014d8-124">The Application Configuration File (ACF)</span></span>](the-application-configuration-file-acf-.md)
-   [<span data-ttu-id="014d8-125">MIDL 編譯器輸出</span><span class="sxs-lookup"><span data-stu-id="014d8-125">MIDL Compiler Output</span></span>](midl-compiler-output.md)

 

 