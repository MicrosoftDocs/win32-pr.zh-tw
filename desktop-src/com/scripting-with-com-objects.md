---
title: 使用 COM 物件編寫腳本
description: 使用 COM 物件編寫腳本
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2019
ms.locfileid: "103677976"
---
# <a name="scripting-with-com-objects"></a><span data-ttu-id="de3ca-103">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="de3ca-103">Scripting with COM Objects</span></span>

<span data-ttu-id="de3ca-104">*指令碼語言* 是一種程式設計語言，可在執行時間由 *腳本引擎* 進行剖析，這是將以該語言撰寫的腳本轉譯成機器碼的元件。</span><span class="sxs-lookup"><span data-stu-id="de3ca-104">A *scripting language* is a programming language that is parsed at run time by a *scripting engine*, a component that translates scripts written in that language into machine code.</span></span> <span data-ttu-id="de3ca-105">每個腳本引擎都會翻譯特定的指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="de3ca-105">Each scripting engine translates a specific scripting language.</span></span> <span data-ttu-id="de3ca-106">*腳本主* 控制項是一種應用程式，例如網頁瀏覽器，它會裝載腳本引擎來執行腳本。</span><span class="sxs-lookup"><span data-stu-id="de3ca-106">A *scripting host* is an application, such as a Web browser, that hosts a scripting engine to run scripts.</span></span> <span data-ttu-id="de3ca-107">如果您的腳本主機支援 COM，您可以撰寫使用 COM 物件的腳本。</span><span class="sxs-lookup"><span data-stu-id="de3ca-107">If your scripting host supports COM, you can write scripts that use COM objects.</span></span> <span data-ttu-id="de3ca-108">下列主題描述支援 COM 物件的腳本主機、通用指令碼語言，以及如何在指令碼語言之間轉譯。</span><span class="sxs-lookup"><span data-stu-id="de3ca-108">The following topics describe scripting hosts that support COM objects, common scripting languages, and how to translate between scripting languages.</span></span>

<span data-ttu-id="de3ca-109">指令碼語言與編譯的語言不同之處在于，它會在執行時間轉譯成機器碼。</span><span class="sxs-lookup"><span data-stu-id="de3ca-109">A scripting language differs from a compiled language in that it is translated into machine code at run time.</span></span> <span data-ttu-id="de3ca-110">這表示當您每次執行腳本時，腳本引擎會先剖析程式碼，然後執行它。</span><span class="sxs-lookup"><span data-stu-id="de3ca-110">This means that each time you run a script, the scripting engine first parses the code and then runs it.</span></span> <span data-ttu-id="de3ca-111">相反地，在編譯期間，編譯的語言（例如 c + +）會轉譯成機器碼一次。</span><span class="sxs-lookup"><span data-stu-id="de3ca-111">In contrast, compiled languages, such as C++, are translated to machine code once, during compilation.</span></span> <span data-ttu-id="de3ca-112">當您執行已編譯的應用程式時，作業系統只會執行先行編譯的程式碼。</span><span class="sxs-lookup"><span data-stu-id="de3ca-112">When you run a compiled application, the operating system simply runs the precompiled code.</span></span>

<span data-ttu-id="de3ca-113">由於腳本引擎必須在每次執行腳本時重新剖析腳本，因此指令碼語言的速度通常會比先行編譯的對應專案更慢且更有效率。</span><span class="sxs-lookup"><span data-stu-id="de3ca-113">Because a scripting engine must reparse a script each time it runs, scripting languages are typically slower and less efficient than their precompiled counterparts.</span></span> <span data-ttu-id="de3ca-114">不過，腳本的優點是容易撰寫和維護。</span><span class="sxs-lookup"><span data-stu-id="de3ca-114">The advantage of scripts, however, is they are easy to write and maintain.</span></span> <span data-ttu-id="de3ca-115">指令碼語言通常比先行編譯語言更簡單，而且當腳本變更時，就不需要重新編譯。</span><span class="sxs-lookup"><span data-stu-id="de3ca-115">Scripting languages are usually simpler than precompiled languages, and when a script changes, it does not need to be recompiled.</span></span> <span data-ttu-id="de3ca-116">針對輕量且快速變更的應用程式（例如網頁），指令碼語言很理想。</span><span class="sxs-lookup"><span data-stu-id="de3ca-116">For lightweight and rapidly changing applications, such as webpages, scripting languages are ideal.</span></span>

<span data-ttu-id="de3ca-117">您可以使用數個主機環境來撰寫使用 COM 物件的腳本，如下所述：</span><span class="sxs-lookup"><span data-stu-id="de3ca-117">There are several host environments in which you can write scripts that use COM objects, as described following:</span></span>

-   [<span data-ttu-id="de3ca-118">在網頁中內嵌 COM 物件</span><span class="sxs-lookup"><span data-stu-id="de3ca-118">Embedding COM Objects in Web Pages</span></span>](embedding-com-objects-in-web-pages.md)
-   [<span data-ttu-id="de3ca-119">使用 Active Server Pages 中的 COM 物件</span><span class="sxs-lookup"><span data-stu-id="de3ca-119">Using COM Objects in Active Server Pages</span></span>](using-com-objects-in-active-server-pages.md)
-   [<span data-ttu-id="de3ca-120">在 Windows Script Host 中使用 COM 物件</span><span class="sxs-lookup"><span data-stu-id="de3ca-120">Using COM Objects in Windows Script Host</span></span>](using-com-objects-in-windows-script-host.md)
-   [<span data-ttu-id="de3ca-121">在自訂應用程式中編寫 COM 物件的腳本</span><span class="sxs-lookup"><span data-stu-id="de3ca-121">Scripting COM Objects in Custom Applications</span></span>](scripting-com-objects-in-custom-applications.md)

<span data-ttu-id="de3ca-122">在前面提到的每個主機環境中，腳本引擎會剖析並執行腳本。</span><span class="sxs-lookup"><span data-stu-id="de3ca-122">In each of the host environments mentioned preceding, a scripting engine parses and runs the script.</span></span> <span data-ttu-id="de3ca-123">因為每個指令碼語言的引擎都是個別的元件，所以您可以藉由加入新的引擎，將新的指令碼語言新增至環境。</span><span class="sxs-lookup"><span data-stu-id="de3ca-123">Because the engine for each scripting language is a separate component, you can add a new scripting language to an environment by adding a new engine.</span></span>

<span data-ttu-id="de3ca-124">最常使用的指令碼語言為：</span><span class="sxs-lookup"><span data-stu-id="de3ca-124">The most commonly used scripting languages are:</span></span>

-   <span data-ttu-id="de3ca-125">Microsoft Visual Basic Scripting Edition (VBScript) ，Visual Basic 的子集。</span><span class="sxs-lookup"><span data-stu-id="de3ca-125">Microsoft Visual Basic Scripting Edition (VBScript), a subset of Visual Basic.</span></span>
-   <span data-ttu-id="de3ca-126">JavaScript 是 Netscape 指令碼語言，先前稱為 LiveScript。</span><span class="sxs-lookup"><span data-stu-id="de3ca-126">JavaScript, the Netscape scripting language, formerly known as LiveScript.</span></span>
-   <span data-ttu-id="de3ca-127">Microsoft JScript 開發軟體，這是 Microsoft 在 ECMA 262 語言規格中的實作為。</span><span class="sxs-lookup"><span data-stu-id="de3ca-127">Microsoft JScript development software, the Microsoft implementation of the ECMA 262 language specification.</span></span>

<span data-ttu-id="de3ca-128">Microsoft 提供適用于 JScript 和 VBScript 的腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="de3ca-128">Microsoft provides scripting engines for JScript and VBScript.</span></span> <span data-ttu-id="de3ca-129">其他軟體公司則提供 ActiveX 腳本引擎，適用于 PerlScript、PScript、Python 等語言。</span><span class="sxs-lookup"><span data-stu-id="de3ca-129">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="de3ca-130">如需詳細資訊，請參閱 [ECMA 262 語言規格](https://www.ecma-international.org/publications/standards/Ecma-262.htm)。</span><span class="sxs-lookup"><span data-stu-id="de3ca-130">For more information see the [ECMA 262 language specification](https://www.ecma-international.org/publications/standards/Ecma-262.htm).</span></span>

<span data-ttu-id="de3ca-131">請注意，大部分的指令碼語言（如 VBScript 和 JScript）無法存取或修改檔案。</span><span class="sxs-lookup"><span data-stu-id="de3ca-131">Note that most scripting languages, such as VBScript and JScript, cannot access or modify files.</span></span> <span data-ttu-id="de3ca-132">這無法防止腳本變更用戶端電腦上的資料。</span><span class="sxs-lookup"><span data-stu-id="de3ca-132">This inability prevents the script from altering data on client computers.</span></span> <span data-ttu-id="de3ca-133">不過，COM 物件沒有這類限制。</span><span class="sxs-lookup"><span data-stu-id="de3ca-133">COM objects, however, have no such limitations.</span></span> <span data-ttu-id="de3ca-134">在用戶端電腦上下載並安裝這些電腦之後，就可以執行任何標準的應用程式動作。</span><span class="sxs-lookup"><span data-stu-id="de3ca-134">Once they are downloaded and installed on client computers, they can perform any standard application action.</span></span> <span data-ttu-id="de3ca-135">因此，使用者只能從受信任的來源下載並執行 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="de3ca-135">Thus, users should only download and run ActiveX controls from trusted sources.</span></span>

<span data-ttu-id="de3ca-136">如需在指令碼語言之間轉換的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="de3ca-136">For information on translating between scripting languages, see the following topics:</span></span>

-   [<span data-ttu-id="de3ca-137">翻譯為 VBScript</span><span class="sxs-lookup"><span data-stu-id="de3ca-137">Translating to VBScript</span></span>](translating-to-vbscript.md)
-   [<span data-ttu-id="de3ca-138">翻譯為 JScript</span><span class="sxs-lookup"><span data-stu-id="de3ca-138">Translating to JScript</span></span>](translating-to-jscript.md)
-   [<span data-ttu-id="de3ca-139">翻譯為 JavaScript</span><span class="sxs-lookup"><span data-stu-id="de3ca-139">Translating to JavaScript</span></span>](translating-to-javascript.md)

 

 




