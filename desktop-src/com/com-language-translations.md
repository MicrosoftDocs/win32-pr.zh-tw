---
title: COM 語言翻譯
description: 使用元件物件模型建立的元件 (COM) 可以在以任何支援 COM 的程式設計語言所撰寫的應用程式中重複使用。 這是因為 COM 是二進位標準，因此與語言無關。
ms.assetid: 89e74768-b7bd-4ab6-9129-9e677a9c14ca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f622b83b998402e82d6cf20975331645362c55e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371864"
---
# <a name="com-language-translations"></a><span data-ttu-id="ed428-104">COM 語言翻譯</span><span class="sxs-lookup"><span data-stu-id="ed428-104">COM Language Translations</span></span>

<span data-ttu-id="ed428-105">使用元件物件模型建立的元件 (COM) 可以在以任何支援 COM 的程式設計語言所撰寫的應用程式中重複使用。</span><span class="sxs-lookup"><span data-stu-id="ed428-105">Components created using the Component Object Model (COM) can be reused in applications written in any programming language that supports COM.</span></span> <span data-ttu-id="ed428-106">這是因為 COM 是二進位標準，因此與語言無關。</span><span class="sxs-lookup"><span data-stu-id="ed428-106">This is because COM is a binary standard and, as such, is language-independent.</span></span>

<span data-ttu-id="ed428-107">COM 物件會以最相關的程式設計語言或語言記載。</span><span class="sxs-lookup"><span data-stu-id="ed428-107">COM objects are documented in the most relevant programming language or languages.</span></span> <span data-ttu-id="ed428-108">例如，在網頁中建立以供使用的物件通常會記載于 Microsoft Visual Basic 開發系統中，而系統層級物件通常會記載于 c + + 中。</span><span class="sxs-lookup"><span data-stu-id="ed428-108">For example, objects that are created for use in webpages are typically documented in the Microsoft Visual Basic development system, whereas system-level objects are typically documented in C++.</span></span> <span data-ttu-id="ed428-109">不過，因為 COM 是語言中立的，所以您不一定要使用撰寫或記錄的相同語言的物件。</span><span class="sxs-lookup"><span data-stu-id="ed428-109">However, because COM is language-neutral, you are not limited to using an object in the same language in which it is written or documented.</span></span> <span data-ttu-id="ed428-110">例如，您可以在 JScript 中撰寫應用程式，以使用在 c + + 中建立並記載于 Visual Basic 中的控制項。</span><span class="sxs-lookup"><span data-stu-id="ed428-110">For example, you can write an application in JScript that uses a control created in C++ and documented in Visual Basic.</span></span>

<span data-ttu-id="ed428-111">下列主題討論程式語言之間的差異，並說明如何將 COM 物件語法從某種語言轉譯成另一種語言。</span><span class="sxs-lookup"><span data-stu-id="ed428-111">The following topics discuss the differences between programming languages and describe how to translate COM object syntax from one language to another.</span></span> <span data-ttu-id="ed428-112">其他主題描述如何在各種指令碼語言和環境中使用 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ed428-112">Additional topics describe how to use COM objects in various scripting languages and environments.</span></span>

-   [<span data-ttu-id="ed428-113">語法差異</span><span class="sxs-lookup"><span data-stu-id="ed428-113">Syntax Differences</span></span>](syntax-differences.md)
-   [<span data-ttu-id="ed428-114">資料類型轉換</span><span class="sxs-lookup"><span data-stu-id="ed428-114">Data Type Conversions</span></span>](data-type-conversions.md)
-   [<span data-ttu-id="ed428-115">IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="ed428-115">IDL Files</span></span>](idl-files.md)
-   [<span data-ttu-id="ed428-116">轉換程式設計語言的 COM 物件語法</span><span class="sxs-lookup"><span data-stu-id="ed428-116">Translating COM Object Syntax for Programming Languages</span></span>](translating-com-object-syntax-for-programming-languages.md)
-   [<span data-ttu-id="ed428-117">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="ed428-117">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)

<span data-ttu-id="ed428-118">其目的是要解決使用 COM 物件時所發生的最常見語言轉譯問題。</span><span class="sxs-lookup"><span data-stu-id="ed428-118">The intent is to address the most common language translation issues that arise when using COM objects.</span></span> <span data-ttu-id="ed428-119">所述的技術和原則適用于任何支援 COM 的程式設計或指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="ed428-119">The techniques and principles described apply to any programming or scripting language that supports COM.</span></span> <span data-ttu-id="ed428-120">因為指令碼語言和程式設計語言代表不同的程式設計架構，所以不會處理指令碼語言與程式設計語言之間的轉譯。</span><span class="sxs-lookup"><span data-stu-id="ed428-120">Because scripting languages and programming languages represent different programming paradigms, translation between scripting languages and programming languages is not addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed428-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed428-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed428-122">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="ed428-122">Component Object Model (COM)</span></span>](component-object-model--com--portal.md)
</dt> </dl>

 

 




