---
title: HLSL 的參考
description: HLSL 參考檔會指定語言特性。 它分成數個部分。
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021835"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="11d84-104">HLSL 的參考</span><span class="sxs-lookup"><span data-stu-id="11d84-104">Reference for HLSL</span></span>

<span data-ttu-id="11d84-105">HLSL 參考檔會指定語言特性。</span><span class="sxs-lookup"><span data-stu-id="11d84-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="11d84-106">它分成數個部分。</span><span class="sxs-lookup"><span data-stu-id="11d84-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="11d84-107">[語言語法 (DIRECTX HLSL) ](dx-graphics-hlsl-language-syntax.md) -HLSL 中的程式設計著色器需要您瞭解語言語法，也就是撰寫 HLSL 程式碼的方式。</span><span class="sxs-lookup"><span data-stu-id="11d84-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="11d84-108">這包括用來宣告和初始化變數、撰寫使用者定義著色器函式的程式碼，以及新增流程式控制制語句，讓您的函式更具強大功能。</span><span class="sxs-lookup"><span data-stu-id="11d84-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="11d84-109">[著色器模型與著色器設定檔](dx-graphics-hlsl-models.md) -HLSL 編譯器會根據著色器模型來實行規則和限制。</span><span class="sxs-lookup"><span data-stu-id="11d84-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="11d84-110">每個頂點著色器中的程式碼、幾何著色器 (如果您使用 Direct3D 10) 和圖元著色器是針對您在編譯時期提供的著色器模型進行驗證。</span><span class="sxs-lookup"><span data-stu-id="11d84-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="11d84-111">[**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL 有許多內建函式。</span><span class="sxs-lookup"><span data-stu-id="11d84-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="11d84-112">這些會經過執行和測試，讓您可以使用它們來瞭解它們已經過調試，而且表現正常。</span><span class="sxs-lookup"><span data-stu-id="11d84-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="11d84-113">如果您選擇撰寫自己的函式，請參閱撰寫使用者定義函數的語言語法一節。</span><span class="sxs-lookup"><span data-stu-id="11d84-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="11d84-114">[Asm 著色器參考](dx9-graphics-reference-asm.md) -您可以用來程式設計和調試著色器的元件指令。</span><span class="sxs-lookup"><span data-stu-id="11d84-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="11d84-115">[D3DCompiler 參考](dx-graphics-d3dcompiler-reference.md) -編譯原始 HLSL 來源。</span><span class="sxs-lookup"><span data-stu-id="11d84-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="11d84-116">[內嵌格式轉換參考](inline-format-conversion-reference.md) -D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="11d84-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="11d84-117">您可以在應用程式中使用這些函式，同時讀取和寫入材質。</span><span class="sxs-lookup"><span data-stu-id="11d84-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="11d84-118">也就是說，您可以執行就地影像編輯。</span><span class="sxs-lookup"><span data-stu-id="11d84-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="11d84-119">若要使用這些內嵌格式轉換函式，請將 D3DX \_ DXGIFormatConvert. .inl 檔案包含在您的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="11d84-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="11d84-120">[附錄 (DIRECTX HLSL) ](dx-graphics-hlsl-appendix.md) -已包含附錄以提供完整性。</span><span class="sxs-lookup"><span data-stu-id="11d84-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="11d84-121">其中包含關鍵字和保留字的清單;這些字組無法當做程式中的識別碼使用。</span><span class="sxs-lookup"><span data-stu-id="11d84-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="11d84-122">它也包含用於參考的語言文法清單。</span><span class="sxs-lookup"><span data-stu-id="11d84-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="11d84-123">[**HLSL 錯誤和警告**](hlsl-errors-and-warnings.md) -提供著色器可傳回的錯誤和警告碼。</span><span class="sxs-lookup"><span data-stu-id="11d84-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11d84-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="11d84-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d84-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="11d84-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="11d84-126">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="11d84-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




