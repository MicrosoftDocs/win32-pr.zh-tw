---
title: MIDL 編譯器錯誤和警告
description: 使用 MIDL 編譯器時，錯誤和警告可能是因為命令列參數不當使用或 IDL 和 ACF 檔的內容所造成。
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft 介面定義語言 MIDL，參考
- MIDL 編譯器 MIDL，錯誤
- 編譯器 MIDL，錯誤
- 錯誤 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839076"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="4b1e1-107">MIDL 編譯器錯誤和警告</span><span class="sxs-lookup"><span data-stu-id="4b1e1-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="4b1e1-108">使用 MIDL 編譯器時，錯誤和警告可能是因為命令列參數不當使用或 IDL 和 ACF 檔的內容所造成。</span><span class="sxs-lookup"><span data-stu-id="4b1e1-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="4b1e1-109">如果錯誤是因為不正確地輸入命令列參數，則錯誤或警告訊息可能會指定一或多個 MIDL 編譯器模式參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b1e1-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="4b1e1-110">例如，當您使用/應用程式設定參數時，您可以在 IDL 檔案中包含某些 ACF 屬性，但如果您在不使用/**應用程式 \_** 設定參數的情況下編譯，則該 idl 檔案將會產生錯誤。**\_**</span><span class="sxs-lookup"><span data-stu-id="4b1e1-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="4b1e1-111">IDL 和 ACF 檔案中的錯誤可以分為兩類：預處理器所攔截到的錯誤，以及編譯器所辨識出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b1e1-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="4b1e1-112">本節列出 MIDL 預處理器和編譯器錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4b1e1-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="4b1e1-113">它也會描述其格式和原因。</span><span class="sxs-lookup"><span data-stu-id="4b1e1-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="4b1e1-114">錯誤和警告訊息格式</span><span class="sxs-lookup"><span data-stu-id="4b1e1-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="4b1e1-115">預處理器錯誤</span><span class="sxs-lookup"><span data-stu-id="4b1e1-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="4b1e1-116">編譯器錯誤</span><span class="sxs-lookup"><span data-stu-id="4b1e1-116">Compiler Errors</span></span>](compiler-errors.md)

 

 




