---
description: 本主題包含程式設計資訊。 下列清單會識別一些可協助您撰寫剖析器的程式設計秘訣。
ms.assetid: 24d3e11f-8281-4464-a2d7-f4f2466e9d9e
title: " (網路監視器) 的程式設計考慮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213104060f7dd3c6b6dbe56d22044508e0878c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692784"
---
# <a name="programming-considerations-network-monitor"></a><span data-ttu-id="a1520-104"> (網路監視器) 的程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="a1520-104">Programming Considerations (Network Monitor)</span></span>

<span data-ttu-id="a1520-105">本主題包含程式設計資訊。</span><span class="sxs-lookup"><span data-stu-id="a1520-105">This topic contains programming information.</span></span> <span data-ttu-id="a1520-106">下列清單會識別一些可協助您撰寫剖析器的程式設計秘訣。</span><span class="sxs-lookup"><span data-stu-id="a1520-106">The following list identifies some programming tips to help you write a parser.</span></span>



|                                                 |                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1520-107">自動安裝剖析器</span><span class="sxs-lookup"><span data-stu-id="a1520-107">Auto-installing your parser</span></span>                     | <span data-ttu-id="a1520-108">執行 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 函式以自動安裝您的剖析器，並更新相關聯的 INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="a1520-108">Implement the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function to automatically install your parser, and update the associated INI files.</span></span> <span data-ttu-id="a1520-109">如果您手動安裝剖析器，則必須手動更新所有相關聯的 INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="a1520-109">If you install your parser manually, you must update all associated INI files manually.</span></span>                                                                                                                                                          |
| <span data-ttu-id="a1520-110">剖析通訊協定屬性</span><span class="sxs-lookup"><span data-stu-id="a1520-110">Parsing protocol properties</span></span>                     | <span data-ttu-id="a1520-111">執行 [**AttachProperties**](attachproperties.md) 函式來剖析通訊協定屬性。</span><span class="sxs-lookup"><span data-stu-id="a1520-111">Implement the [**AttachProperties**](attachproperties.md) function to parse the protocol properties.</span></span> <span data-ttu-id="a1520-112">當您附加屬性實例時，請避免使用 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 函式，並將它用於非位元組對齊的資料，或必須解碼的資料。</span><span class="sxs-lookup"><span data-stu-id="a1520-112">Avoid using the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you attach a property instance, and use it for only non byte-aligned data, or data that must be decoded.</span></span> <span data-ttu-id="a1520-113">附加屬性是指將屬性實例對應到捕捉中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="a1520-113">Attaching properties refers to mapping a property instance to a specific location in a capture.</span></span> |
| <span data-ttu-id="a1520-114">剖析框架之間分割的通訊協定</span><span class="sxs-lookup"><span data-stu-id="a1520-114">Parsing protocols that are split between frames</span></span> | <span data-ttu-id="a1520-115">假設通訊協定的每個部分都已在畫面格內完成，並假設使用者呼叫通訊協定聯合工具，將這些元件合併成一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a1520-115">Assume that each piece of the protocol is complete within a frame, and assume that the user calls the Protocol Coalesce tool to combine the pieces into one protocol.</span></span> <span data-ttu-id="a1520-116">剖析通訊協定時，請不要回頭查看先前的畫面格，並避免嘗試重建在畫面格之間分割的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a1520-116">Do not look back at a previous frame when parsing a protocol, and avoid trying to reconstruct a protocol that is split between frames.</span></span>                                                                                              |
| <span data-ttu-id="a1520-117">格式化顯示的資料</span><span class="sxs-lookup"><span data-stu-id="a1520-117">Formatting displayed data</span></span>                       | <span data-ttu-id="a1520-118">呼叫 [**FormatPropertyInstance**](formatpropertyinstance.md) 函式，以使用一般格式子來格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="a1520-118">Call the [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the generic formatter to format the data displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="a1520-119">避免撰寫 UI 顯示資料的自訂格式器。</span><span class="sxs-lookup"><span data-stu-id="a1520-119">Avoid writing a custom formatter for UI display data.</span></span> <span data-ttu-id="a1520-120">不過，您可以呼叫自訂格式器，為您正在剖析的通訊協定建立 [*摘要屬性*](s.md) 行。</span><span class="sxs-lookup"><span data-stu-id="a1520-120">However, you can call a custom formatter to create a [*summary property*](s.md) line for the protocol you are parsing.</span></span>            |
| <span data-ttu-id="a1520-121">使用 CCAlloc</span><span class="sxs-lookup"><span data-stu-id="a1520-121">Using CCAlloc</span></span>                                   | <span data-ttu-id="a1520-122">當您想要網路監視器以每個捕獲為基礎來配置資料時，請使用 CCAlloc。</span><span class="sxs-lookup"><span data-stu-id="a1520-122">Use CCAlloc when you want Network Monitor to allocate data on a per-capture basis.</span></span> <span data-ttu-id="a1520-123">網路監視器不會指定框架呼叫剖析器的順序。</span><span class="sxs-lookup"><span data-stu-id="a1520-123">Network Monitor does not specify the order that frames call the parser.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="a1520-124">保持剖析器無狀態</span><span class="sxs-lookup"><span data-stu-id="a1520-124">Keeping a parser stateless</span></span>                      | <span data-ttu-id="a1520-125">將剖析器作業保持無狀態，因為當網路監視器剖析捕捉時，不會以特定順序將框架傳遞給剖析器。</span><span class="sxs-lookup"><span data-stu-id="a1520-125">Keep parser operation stateless because when Network Monitor parses a capture, it does not pass the frames to the parser in a specific order.</span></span> <span data-ttu-id="a1520-126">基於這個理由，建議您不要保留全域資料。</span><span class="sxs-lookup"><span data-stu-id="a1520-126">For this reason, it is recommended that you do not retain global data.</span></span>                                                                                                                                                                                      |



 

 

 



