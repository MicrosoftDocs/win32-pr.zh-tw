---
title: Windows Media Player 物件模型參考
description: Windows Media Player 物件模型參考
ms.assetid: af313b94-230b-47d7-a3ad-7e23b669886f
keywords:
- Windows Media Player，物件模型
- Windows Media Player 行動裝置，物件模型
- Windows Media Player 物件模型，參考
- 物件模型，參考
- ActiveX 控制項，參考
- Windows Media Player ActiveX 控制項，參考
- Windows Media Player Mobile ActiveX 控制項，參考
- 物件模型參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6128ff3f69968ddf4f8a35955907a18876ef090
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021972"
---
# <a name="windows-media-player-object-model-reference"></a><span data-ttu-id="b6646-111">Windows Media Player 物件模型參考</span><span class="sxs-lookup"><span data-stu-id="b6646-111">Windows Media Player Object Model Reference</span></span>

<span data-ttu-id="b6646-112">Windows Media Player 物件模型參考章節包含 Windows Media Player ActiveX 控制項物件模型的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b6646-112">The Windows Media Player Object Model Reference sections contain detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="b6646-113">物件模型提供的介面可讓開發人員將 Windows Media Player 功能新增至網頁、c + + 程式和 .NET 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6646-113">The object model provides interfaces that let developers add Windows Media Player functionality to webpages, C++ programs, and .NET applications.</span></span>

<span data-ttu-id="b6646-114">腳本的物件模型參考會以設計用來搭配 Microsoft JScript 等指令碼語言使用的樣式呈現，而它會以物件的相關屬性、方法和事件來記錄物件模型。</span><span class="sxs-lookup"><span data-stu-id="b6646-114">The Object Model Reference for Scripting is presented in a style designed for use with script languages like Microsoft JScript, and it documents the object model in terms of objects with their associated properties, methods, and events.</span></span>

<span data-ttu-id="b6646-115">C + + 的物件模型參考提供 COM 介面的檔，c + + 程式設計人員可以使用這些介面與 Windows Media Player 的 ActiveX 控制項或 Windows Media Player 的行動 ActiveX 控制項進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b6646-115">The Object Model Reference for C++ provides documentation for COM interfaces that C++ programmers can use to communicate with the Windows Media Player ActiveX control or the Windows Media Player Mobile ActiveX control.</span></span> <span data-ttu-id="b6646-116">這些介面大多是由 Windows Media Player 控制項所執行，並由 c + + 應用程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="b6646-116">Most of these interfaces are implemented by Windows Media Player control and called by the C++ application.</span></span> <span data-ttu-id="b6646-117">不過，某些介面 (例如， **IWMPEvents** 和 **IWMPRemoteMediaServices**) 是由 c + + 應用程式所執行，並由 Windows Media Player 控制項呼叫。</span><span class="sxs-lookup"><span data-stu-id="b6646-117">However, some of the interfaces (for example, **IWMPEvents** and **IWMPRemoteMediaServices**) are implemented by the C++ application and called by the Windows Media Player control.</span></span>

<span data-ttu-id="b6646-118">Visual Basic .NET 和 c # 的物件模型參考會提供 **AxWindowsMediaPlayer** 物件的屬性、方法和事件的相關檔，以及適用于 Windows Media Player ActiveX 控制項的介面，該控制項可透過 Visual Studio .NET 2002 或更新版本中編碼的解決方案中的 COM 互通性取得。</span><span class="sxs-lookup"><span data-stu-id="b6646-118">The Object Model Reference for Visual Basic .NET and C# provides documentation for the properties, methods, and events of the **AxWindowsMediaPlayer** object and for interfaces to the Windows Media Player ActiveX control that are available through COM interoperability in a solution coded in Visual Studio .NET 2002 or later.</span></span>

<span data-ttu-id="b6646-119">Windows Media Player 物件模型參考包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b6646-119">The Windows Media Player Object Model Reference contains the following sections.</span></span>



| <span data-ttu-id="b6646-120">區段</span><span class="sxs-lookup"><span data-stu-id="b6646-120">Section</span></span>                                                                                                        | <span data-ttu-id="b6646-121">描述</span><span class="sxs-lookup"><span data-stu-id="b6646-121">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6646-122">腳本的物件模型參考</span><span class="sxs-lookup"><span data-stu-id="b6646-122">Object Model Reference for Scripting</span></span>](object-model-reference-for-scripting.md)                               | <span data-ttu-id="b6646-123">提供物件模型可供指令碼語言使用之屬性、方法和事件的參考檔集。</span><span class="sxs-lookup"><span data-stu-id="b6646-123">Provides reference documentation for the properties, methods, and events that the object model makes available to scripting languages.</span></span> <span data-ttu-id="b6646-124">這項資訊也適用于 Visual Basic 6.0 程式設計。</span><span class="sxs-lookup"><span data-stu-id="b6646-124">This information is also useful for Visual Basic 6.0 programming.</span></span> |
| [<span data-ttu-id="b6646-125">C + + 的物件模型參考</span><span class="sxs-lookup"><span data-stu-id="b6646-125">Object Model Reference for C++</span></span>](object-model-reference-for-c.md)                                             | <span data-ttu-id="b6646-126">提供 c + + 介面的參考檔。</span><span class="sxs-lookup"><span data-stu-id="b6646-126">Provides reference documentation for C++ interfaces.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="b6646-127">Visual Basic .NET 和 C 的物件模型參考#</span><span class="sxs-lookup"><span data-stu-id="b6646-127">Object Model Reference for Visual Basic .NET and C#</span></span>](object-model-reference-for-visual-basic--net-and-c.md) | <span data-ttu-id="b6646-128">提供可透過 COM 互通性 Visual Basic .NET 和 c # 程式設計人員使用之物件和介面的參考檔。</span><span class="sxs-lookup"><span data-stu-id="b6646-128">Provides reference documentation for objects and interfaces available to Visual Basic .NET and C# programmers through COM interoperability.</span></span>                                                             |
| [<span data-ttu-id="b6646-129">屬性參考</span><span class="sxs-lookup"><span data-stu-id="b6646-129">Attribute Reference</span></span>](attribute-reference.md)                                                                 | <span data-ttu-id="b6646-130">提供 Windows Media Player SDK 開發人員感興趣之中繼資料屬性的參考檔。</span><span class="sxs-lookup"><span data-stu-id="b6646-130">Provides reference documentation for metadata attributes that are of interest to Windows Media Player SDK developers.</span></span>                                                                                    |
| [<span data-ttu-id="b6646-131">列舉類型</span><span class="sxs-lookup"><span data-stu-id="b6646-131">Enumeration Types</span></span>](enumeration-types.md)                                                                     | <span data-ttu-id="b6646-132">提供 c + + 和 .NET 介面所使用之列舉類型的參考檔集。</span><span class="sxs-lookup"><span data-stu-id="b6646-132">Provides reference documentation for the enumeration types that are used by the C++ and .NET interfaces.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="b6646-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6646-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6646-134">**Windows Media Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="b6646-134">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




