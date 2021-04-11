---
description: 剖析器是在延遲的捕獲中檢查資料的網路監視器元件，並將特定的通訊協定資訊傳遞給呼叫剖析器的應用程式。 剖析器是被動的，因為它只會在網路監視器或專家呼叫它時運作。
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: 剖析器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847727"
---
# <a name="parser"></a><span data-ttu-id="a3479-104">剖析器</span><span class="sxs-lookup"><span data-stu-id="a3479-104">Parser</span></span>

<span data-ttu-id="a3479-105">剖析器是在 [*延遲的捕獲*](d.md)中檢查資料的網路監視器元件，並將特定的通訊協定資訊傳遞給呼叫剖析器的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a3479-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="a3479-106">剖析器是被動的，因為它只會在網路監視器或 [*專家*](e.md) 呼叫它時運作。</span><span class="sxs-lookup"><span data-stu-id="a3479-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="a3479-107">每個剖析器都會識別一個通訊協定，而且通常會在它自己的剖析器 DLL 內實作為剖析器。</span><span class="sxs-lookup"><span data-stu-id="a3479-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="a3479-108">不過，剖析器 DLL 可以包含多個剖析器，這表示一個 DLL 可用來偵測一個以上的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a3479-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="a3479-109">傳遞給剖析器的資料是取自延遲的 [*捕獲*](d.md)，並以每個畫面格為基礎傳遞給剖析器。</span><span class="sxs-lookup"><span data-stu-id="a3479-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="a3479-110">您無法剖析即時捕捉。</span><span class="sxs-lookup"><span data-stu-id="a3479-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="a3479-111">若要剖析框架中的資料，剖析器必須辨識通訊協定實例、識別存在於通訊協定實例中的屬性，並將屬性定義附加至每個屬性。</span><span class="sxs-lookup"><span data-stu-id="a3479-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="a3479-112">請注意，框架只會包含資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a3479-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="a3479-113">此框架不包含指出資料所代表之通訊協定或通訊協定屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="a3479-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="a3479-114">下圖顯示包含通訊協定實例的框架。</span><span class="sxs-lookup"><span data-stu-id="a3479-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![包含通訊協定實例的框架](images/parser1.png)

<span data-ttu-id="a3479-116">如果網路監視器要在 UI 中顯示剖析的資料，剖析器必須將資料格式化。</span><span class="sxs-lookup"><span data-stu-id="a3479-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="a3479-117">不過，某些專家會以程式設計方式使用剖析器輸出，而不會在網路監視器 UI 中顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="a3479-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="a3479-118">顯示的資料包含剖析器定義的資料，以及捕捉中的資料。</span><span class="sxs-lookup"><span data-stu-id="a3479-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="a3479-119">例如，剖析器通常會提供所顯示內容的名稱，以及捕捉中與屬性相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="a3479-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="a3479-120">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="a3479-120">For information about</span></span>                                         | <span data-ttu-id="a3479-121">請參閱</span><span class="sxs-lookup"><span data-stu-id="a3479-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="a3479-122">必須在剖析器 DLL 內實作為進入點。</span><span class="sxs-lookup"><span data-stu-id="a3479-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="a3479-123">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="a3479-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="a3479-124">如何執行剖析器 DLL 匯出函數。</span><span class="sxs-lookup"><span data-stu-id="a3479-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="a3479-125">撰寫通訊協定剖析器</span><span class="sxs-lookup"><span data-stu-id="a3479-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="a3479-126">剖析器使用哪些函數和結構。</span><span class="sxs-lookup"><span data-stu-id="a3479-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="a3479-127">剖析器函式和結構</span><span class="sxs-lookup"><span data-stu-id="a3479-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



