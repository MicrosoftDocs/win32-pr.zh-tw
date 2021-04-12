---
description: 您可以使用手寫的正則運算式所組成的語言模型來定義自訂輸入範圍，並將其指派給欄位。例如，如果您要為倉儲元件建立資料庫應用程式，並希望使用者能夠使用 Tablet PC 輸入面板的手寫板來輸入零件編號。 如果元件編號語法包含三個字母，後面接著四個數字，後面接著另一個字母 (例如，ABC1234D) ，則手寫辨識器會因為未在語言模型中定義，而難以辨識這類輸入。 沒有任何預先定義的模擬程式對應到這類語法，Microsoft 也不會針對應用程式可能需要的每個可能欄位包含語法。 手寫的正則運算式提供簡單的方法，讓應用程式針對特定的特殊用途欄位定義自己的語言模型。注意：在使用已啟用筆墨的應用程式中使用 RecognizerCoNtext 物件的「模擬」屬性時，您無法在正則運算式中使用第1版的 factoids。
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: 使用正則運算式的自訂輸入範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026026"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="a53e5-106">使用正則運算式的自訂輸入範圍</span><span class="sxs-lookup"><span data-stu-id="a53e5-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="a53e5-107">您可以使用手寫的正則運算式所組成的語言模型來定義自訂輸入範圍，並將其指派給欄位。</span><span class="sxs-lookup"><span data-stu-id="a53e5-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="a53e5-108">例如，如果您要為倉儲元件建立資料庫應用程式，並希望使用者能夠使用 Tablet PC 輸入面板的手寫板來輸入零件編號。</span><span class="sxs-lookup"><span data-stu-id="a53e5-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="a53e5-109">如果元件編號語法包含三個字母，後面接著四個數字，後面接著另一個字母 (例如，ABC1234D) ，則手寫辨識器會因為未在語言模型中定義，而難以辨識這類輸入。</span><span class="sxs-lookup"><span data-stu-id="a53e5-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="a53e5-110">沒有任何預先定義的模擬程式對應到這類語法，Microsoft 也不會針對應用程式可能需要的每個可能欄位包含語法。</span><span class="sxs-lookup"><span data-stu-id="a53e5-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="a53e5-111">手寫的正則運算式提供簡單的方法，讓應用程式針對特定的特殊用途欄位定義自己的語言模型。</span><span class="sxs-lookup"><span data-stu-id="a53e5-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="a53e5-112">在使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件之 [[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)] 屬性的啟用筆墨的應用程式中工作時，您無法在正則運算式中使用第1版的 factoids。</span><span class="sxs-lookup"><span data-stu-id="a53e5-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



