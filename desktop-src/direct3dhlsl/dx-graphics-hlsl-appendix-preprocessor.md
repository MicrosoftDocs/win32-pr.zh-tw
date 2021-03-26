---
title: '預處理器指示詞 (HLSL) '
description: 預處理器指示詞（例如 \ 定義和 \ ifdef）通常用來讓來來源程式在不同的執行環境中變得更容易變更和編譯。
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685340"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="9eeff-103">預處理器指示詞 (HLSL) </span><span class="sxs-lookup"><span data-stu-id="9eeff-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="9eeff-104">預處理器指示詞（例如[ \# define](dx-graphics-hlsl-appendix-pre-define.md)和[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)）通常用來讓來來源程式在不同的執行環境中變得更容易變更和編譯。</span><span class="sxs-lookup"><span data-stu-id="9eeff-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="9eeff-105">原始程式檔中的指示詞會指示前置處理器執行特定動作。</span><span class="sxs-lookup"><span data-stu-id="9eeff-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="9eeff-106">例如，前置處理器可以取代文字中的語彙基元、將其他檔案的內容插入原始程式檔，或是透過移除文字區段來隱藏編譯檔案的一部分。</span><span class="sxs-lookup"><span data-stu-id="9eeff-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="9eeff-107">在巨集展開之前，會辨識並執行前置處理器程式行。</span><span class="sxs-lookup"><span data-stu-id="9eeff-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="9eeff-108">因此，如果巨集展開成類似前置處理器命令的程式碼，前置處理器就無法辨識該命令。</span><span class="sxs-lookup"><span data-stu-id="9eeff-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="9eeff-109">除了不支援逸出序列以外，前置處理器陳述式使用的字元集與原始程式檔陳述式使用的相同。</span><span class="sxs-lookup"><span data-stu-id="9eeff-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="9eeff-110">前置處理器陳述式中使用的字元集與執行字元集相同。</span><span class="sxs-lookup"><span data-stu-id="9eeff-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="9eeff-111">前置處理器也會辨識負數字元值。</span><span class="sxs-lookup"><span data-stu-id="9eeff-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="9eeff-112">HLSL 預處理器會辨識下列指示詞：</span><span class="sxs-lookup"><span data-stu-id="9eeff-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="9eeff-113">\#定義</span><span class="sxs-lookup"><span data-stu-id="9eeff-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="9eeff-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="9eeff-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="9eeff-115">\#else</span><span class="sxs-lookup"><span data-stu-id="9eeff-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="9eeff-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="9eeff-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="9eeff-117">\#錯誤</span><span class="sxs-lookup"><span data-stu-id="9eeff-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="9eeff-118">\#如果</span><span class="sxs-lookup"><span data-stu-id="9eeff-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="9eeff-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="9eeff-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="9eeff-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="9eeff-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="9eeff-121">\#包括</span><span class="sxs-lookup"><span data-stu-id="9eeff-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="9eeff-122">\#線</span><span class="sxs-lookup"><span data-stu-id="9eeff-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="9eeff-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="9eeff-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="9eeff-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="9eeff-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="9eeff-125">數位記號 (\#) 必須是包含指示詞的行上的第一個非空白字元空白字元; 在數位記號與指示詞的第一個字母之間可以出現空白字元。</span><span class="sxs-lookup"><span data-stu-id="9eeff-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="9eeff-126">某些指示詞會包含引數或值。</span><span class="sxs-lookup"><span data-stu-id="9eeff-126">Some directives include arguments or values.</span></span> <span data-ttu-id="9eeff-127">指示詞後面的任何文字 (除了屬於指示詞一部分的引數或值以外，) 前面必須加上單行批註分隔符號 (//) 或以批註分隔符號括住 (/ \* \* /) 。</span><span class="sxs-lookup"><span data-stu-id="9eeff-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="9eeff-128">包含預處理器指示詞的行，可以透過反斜線 (緊接在行尾標記之前繼續 \) 。</span><span class="sxs-lookup"><span data-stu-id="9eeff-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\).</span></span>

<span data-ttu-id="9eeff-129">前置處理器指示詞可以出現在原始程式檔的任何位置，但是這只會套用至原始程式檔的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="9eeff-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eeff-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eeff-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eeff-131">附錄 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="9eeff-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




