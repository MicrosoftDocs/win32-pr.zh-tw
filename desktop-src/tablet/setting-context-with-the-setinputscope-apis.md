---
description: 在未啟用筆墨的應用程式中設定內容的建議程式設計技術，是使用 SetInputScope 函式，將內容與應用程式中的欄位產生關聯。
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: 使用 SetInputScope Api 設定內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987000"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="04077-103">使用 SetInputScope Api 設定內容</span><span class="sxs-lookup"><span data-stu-id="04077-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="04077-104">在未啟用筆墨的應用程式中設定內容的建議程式設計技術，是使用 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 函式，將內容與應用程式中的欄位產生關聯。</span><span class="sxs-lookup"><span data-stu-id="04077-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="04077-105">Microsoft Windows XP Tablet PC Edition 開發工具組1.7 是第一個提供 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)的 microsoft windows 版本。</span><span class="sxs-lookup"><span data-stu-id="04077-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="04077-106">Windows Vista 也提供這些功能的支援。</span><span class="sxs-lookup"><span data-stu-id="04077-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="04077-107">**SetInputScope** 定義是在 InputScope .Idl 和 InputScope 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="04077-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="04077-108">如需詳細資訊，請參閱 [文字服務架構](../tsf/text-services-framework.md)。</span><span class="sxs-lookup"><span data-stu-id="04077-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="04077-109">[**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)函式是針對未啟用筆墨的控制項和應用程式設定內容的建議方式。</span><span class="sxs-lookup"><span data-stu-id="04077-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="04077-110">一般輸入範圍</span><span class="sxs-lookup"><span data-stu-id="04077-110">Common Input Scopes</span></span>

<span data-ttu-id="04077-111">您可以使用 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) 函式和 [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) 列舉中所述的一組已定義通用輸入範圍，來改善 Microsoft 手寫辨識器的辨識精確度。</span><span class="sxs-lookup"><span data-stu-id="04077-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="04077-112">英文版的辨識器 (美國) 、英文 (英國) 、德文、法文、義大利文、西班牙文、荷蘭文及葡萄牙文，目前支援搭配 [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)使用一般輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="04077-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
