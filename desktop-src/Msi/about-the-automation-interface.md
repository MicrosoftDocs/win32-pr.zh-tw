---
description: 最初必須建立安裝程式物件，以載入透過 COM 存取安裝程式元件所需的自動化支援。
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: 關於 Automation 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192476"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="3e43d-103">關於 Automation 介面</span><span class="sxs-lookup"><span data-stu-id="3e43d-103">About the Automation Interface</span></span>

<span data-ttu-id="3e43d-104">最初必須建立 [**安裝程式物件**](installer-object.md) ，以載入透過 COM 存取安裝程式元件所需的自動化支援。</span><span class="sxs-lookup"><span data-stu-id="3e43d-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="3e43d-105">這個物件會提供包裝函式來建立最上層的物件，並存取其方法。</span><span class="sxs-lookup"><span data-stu-id="3e43d-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="3e43d-106">這些包裝函式只會提供參數轉譯，以與 Microsoft Visual Basic 一致的方式公開安裝程式功能，而不會變更方法的行為。</span><span class="sxs-lookup"><span data-stu-id="3e43d-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="3e43d-107">可能的話，會將一組 Get 和 Set c + + 方法公開給 Visual Basic，以做為單一屬性。</span><span class="sxs-lookup"><span data-stu-id="3e43d-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="3e43d-108">在某些情況下，採用索引引數的 c + + 方法會公開為索引屬性。</span><span class="sxs-lookup"><span data-stu-id="3e43d-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="3e43d-109">許多 c + + 方法會透過參數傳回結果，因為傳回值是用於錯誤傳回。</span><span class="sxs-lookup"><span data-stu-id="3e43d-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="3e43d-110">不過，在 Visual Basic 中，錯誤是由個別的機制處理，而結果一律會傳入傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e43d-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="3e43d-111">如需使用 automation 和建立安裝程式物件的詳細資訊，請參閱 [使用 Automation 介面](using-the-automation-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="3e43d-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="3e43d-112">如需 Windows Installer 物件的參考資料，請參閱 [Automation 介面參考](automation-interface-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="3e43d-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e43d-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e43d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e43d-114">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="3e43d-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



