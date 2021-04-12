---
description: 錯誤記錄總覽
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: 錯誤記錄總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109080"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="6e613-103">錯誤記錄總覽</span><span class="sxs-lookup"><span data-stu-id="6e613-103">Overview of Error Logging</span></span>

<span data-ttu-id="6e613-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6e613-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6e613-105">為了讓應用程式在處理錯誤時有最大的彈性， [DirectShow 編輯服務](directshow-editing-services.md) 會使用回呼機制。</span><span class="sxs-lookup"><span data-stu-id="6e613-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="6e613-106">您的應用程式會執行記錄錯誤的方法。</span><span class="sxs-lookup"><span data-stu-id="6e613-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="6e613-107">在執行時間，如果發生錯誤，DES 會呼叫您提供的方法。</span><span class="sxs-lookup"><span data-stu-id="6e613-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="6e613-108">方法會使用描述錯誤的參數。</span><span class="sxs-lookup"><span data-stu-id="6e613-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="6e613-109">使用此資訊的方法是由您決定。</span><span class="sxs-lookup"><span data-stu-id="6e613-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="6e613-110"> (應該儘快傳回，否則可能會干擾程式的執行。 ) </span><span class="sxs-lookup"><span data-stu-id="6e613-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="6e613-111">錯誤記錄回呼方法包含在 COM 介面 [**IAMErrorLog**](iamerrorlog.md)中。</span><span class="sxs-lookup"><span data-stu-id="6e613-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="6e613-112">您的應用程式必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="6e613-112">Your application must implement this interface.</span></span> <span data-ttu-id="6e613-113">如同所有的 COM 介面， **IAMErrorLog** 會繼承 **IUnknown** 介面，因此您的應用程式也必須執行該介面。</span><span class="sxs-lookup"><span data-stu-id="6e613-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="6e613-114">您有數個選項可執行這些 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="6e613-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="6e613-115">您可以使用 Active Template Library (ATL) ，它會提供 **IUnknown** 方法的庫存實作為。</span><span class="sxs-lookup"><span data-stu-id="6e613-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="6e613-116">DirectShow 也提供 c + + 基類 [**CUnknown**](cunknown.md)，可讓您輕鬆地執行 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="6e613-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="6e613-117">如需使用 **CUnknown** 的詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="6e613-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="6e613-118">本文中的範例程式碼會定義獨立的 c + + 類別，以同時執行 **IUnknown** 和 **IAMErrorLog**。</span><span class="sxs-lookup"><span data-stu-id="6e613-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="6e613-119">結果不是真正的 COM 物件，因為它不支援 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="6e613-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="6e613-120">不過，這種方法適用于範例的目的。</span><span class="sxs-lookup"><span data-stu-id="6e613-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e613-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e613-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e613-122">記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="6e613-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



