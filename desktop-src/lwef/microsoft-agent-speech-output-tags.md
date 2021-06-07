---
title: Microsoft 代理程式語音輸出標記
description: Microsoft 代理程式語音輸出標記
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386797"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="6e6a2-103">Microsoft 代理程式語音輸出標記</span><span class="sxs-lookup"><span data-stu-id="6e6a2-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="6e6a2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6e6a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6e6a2-105">Microsoft 代理程式服務支援透過在語音文字字串中插入的特殊標記來修改語音輸出。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="6e6a2-106">這些標記可協助您變更字元輸出運算式的特性。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="6e6a2-107">語音輸出標記會使用下列語法規則：</span><span class="sxs-lookup"><span data-stu-id="6e6a2-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="6e6a2-108">所有標記的開頭和結尾都是反斜線字元 (\\) 。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-108">All tags begin and end with a backslash character (\\).</span></span>
-   <span data-ttu-id="6e6a2-109">標記中未啟用單一反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="6e6a2-110">若要在標記的文字參數中包含反斜線字元，請使用雙反斜線 (\\ \\) 。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\\).</span></span>
-   <span data-ttu-id="6e6a2-111">標記不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-111">Tags are case-insensitive.</span></span> <span data-ttu-id="6e6a2-112">例如， \\ pit 與 \\ \\ pit 相同 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="6e6a2-113">標記與空白字元相依。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="6e6a2-114">例如， \\ rst 與 \\ \\ rst 不同 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="6e6a2-115">除非另一個標記另有指定或修改，否則語音輸出會將標記所設定的特性保留在單一 [**說話**](speak-method.md) 方法中指定的文字內。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="6e6a2-116">語音輸出會在 **說話** 方法完成之後，透過使用者定義的參數自動重設。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="6e6a2-117">某些標記包含加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-117">Some tags include quoted strings.</span></span> <span data-ttu-id="6e6a2-118">針對某些程式設計語言（例如 Visual Basic Scripting Edition (VBScript) 和 Visual Basic），這表示您可能必須使用兩個引號來指定標記的參數，或串連雙引號字元作為字串的一部分。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="6e6a2-119">後者會顯示在此 Visual Basic 範例中：</span><span class="sxs-lookup"><span data-stu-id="6e6a2-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="6e6a2-120">若為 C、c + + 和 JAVA™程式設計，請在反斜線和雙引號前面加上反斜線。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="6e6a2-121">例如︰</span><span class="sxs-lookup"><span data-stu-id="6e6a2-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="6e6a2-122">針對支援雙位元組字元集 (DBCS) 字元的外部語言，您可以使用雙位元組字元來指定字串參數。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="6e6a2-123">但是，針對用來定義標記的所有其他參數和字元（包括標記本身），請使用單一位元組字元。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="6e6a2-124">支援的標記如下：</span><span class="sxs-lookup"><span data-stu-id="6e6a2-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="6e6a2-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="6e6a2-126">**環 磷 醯 胺**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="6e6a2-127">**Emp**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="6e6a2-128">**Lst**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="6e6a2-129">**地圖**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="6e6a2-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="6e6a2-131">**保羅**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="6e6a2-132">**坑**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="6e6a2-133">**Rst**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="6e6a2-134">**Spd**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="6e6a2-135">**卷**</span><span class="sxs-lookup"><span data-stu-id="6e6a2-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="6e6a2-136">這些標記主要是設計來調整文字轉換語音 (TTS) 產生的輸出。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="6e6a2-137">只有 [**Mrk**](mrk-tag.md) 和 [**Map**](map-tag.md) 標記可以與以檔案為基礎的聲音輸出搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="6e6a2-138">Microsoft 代理程式不支援 Microsoft 語音 SDK 中記載的所有標記。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="6e6a2-139">參數也會根據選取的 TTS 引擎而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="6e6a2-140">您可以使用 [**TTSModeID**](ttsmodeid-property.md)來設定特定的 TTS 引擎。</span><span class="sxs-lookup"><span data-stu-id="6e6a2-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




