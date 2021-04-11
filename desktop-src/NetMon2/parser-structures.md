---
description: 本章節描述您可以用來開發剖析器的結構。 您可以用來開發剖析器和功能的函式會使用這些結構來開發剖析器或專家。
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: 剖析器結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945497"
---
# <a name="parser-structures"></a><span data-ttu-id="5c2bf-104">剖析器結構</span><span class="sxs-lookup"><span data-stu-id="5c2bf-104">Parser Structures</span></span>

<span data-ttu-id="5c2bf-105">本章節描述您可以用來開發剖析器的結構。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="5c2bf-106">您可以用來開發剖析器和功能的函式會使用這些結構來開發剖析器或專家。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="5c2bf-107">結構</span><span class="sxs-lookup"><span data-stu-id="5c2bf-107">Structure</span></span>                                 | <span data-ttu-id="5c2bf-108">Description</span><span class="sxs-lookup"><span data-stu-id="5c2bf-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c2bf-109">MACFRAME</span><span class="sxs-lookup"><span data-stu-id="5c2bf-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="5c2bf-110">定義最常使用的初始通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="5c2bf-111">E</span><span class="sxs-lookup"><span data-stu-id="5c2bf-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="5c2bf-112">指定剖析器 DLL 進入點的指標。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="5c2bf-113">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="5c2bf-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="5c2bf-114">指定遵循目前通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="5c2bf-115">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="5c2bf-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="5c2bf-116">指定遵循目前通訊協定的通訊協定組。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="5c2bf-117">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="5c2bf-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="5c2bf-118">指定將通訊協定交給目前的通訊協定，或目前的通訊協定所用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="5c2bf-119">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="5c2bf-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="5c2bf-120">指定一組送出目前通訊協定的通訊協定，或目前通訊協定所要關閉的通訊協定組。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="5c2bf-121">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="5c2bf-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="5c2bf-122">指定剖析器 DLL 中的剖析器數目和每個剖析器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="5c2bf-123">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="5c2bf-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="5c2bf-124">指定特定剖析器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="5c2bf-125">標示為 \_ 位</span><span class="sxs-lookup"><span data-stu-id="5c2bf-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="5c2bf-126">指定控制碼、位欄位或旗標。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="5c2bf-127">標記的 \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="5c2bf-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="5c2bf-128">指定 **位元組** 標籤組。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="5c2bf-129">標記的 \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5c2bf-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="5c2bf-130">指定 **DWORD** 標籤組。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="5c2bf-131">標示為 \_ WORD</span><span class="sxs-lookup"><span data-stu-id="5c2bf-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="5c2bf-132">指定 **單字** 標籤組。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="5c2bf-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="5c2bf-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="5c2bf-134">指定通訊協定剖析器所需的屬性來描述畫面格。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="5c2bf-135">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="5c2bf-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="5c2bf-136">指定框架中屬性的實例。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="5c2bf-137">PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="5c2bf-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="5c2bf-138">指定自由格式的擴充屬性實例。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="5c2bf-139">PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="5c2bf-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="5c2bf-140">指定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="5c2bf-141">範圍</span><span class="sxs-lookup"><span data-stu-id="5c2bf-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="5c2bf-142">指定數位的範圍。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="5c2bf-143">SET</span><span class="sxs-lookup"><span data-stu-id="5c2bf-143">SET</span></span>](set.md)                            | <span data-ttu-id="5c2bf-144">指定屬性值的資料表。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="5c2bf-145">如需用於開發剖析器 Dll 之函數的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="5c2bf-146">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="5c2bf-146">For information about</span></span>                                         | <span data-ttu-id="5c2bf-147">請參閱</span><span class="sxs-lookup"><span data-stu-id="5c2bf-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5c2bf-148">剖析器 Dll 匯出的函式。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="5c2bf-149">剖析器 DLL 匯出函數</span><span class="sxs-lookup"><span data-stu-id="5c2bf-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="5c2bf-150">您可以用來開發剖析器 Dll 的函式。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="5c2bf-151">剖析器函式</span><span class="sxs-lookup"><span data-stu-id="5c2bf-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="5c2bf-152">您可以用來開發剖析器和專家 Dll 的函式。</span><span class="sxs-lookup"><span data-stu-id="5c2bf-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="5c2bf-153">專家和剖析器一般函數</span><span class="sxs-lookup"><span data-stu-id="5c2bf-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



