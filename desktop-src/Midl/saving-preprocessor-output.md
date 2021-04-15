---
title: 正在儲存預處理器輸出
description: 查看預處理器輸出可能是有效的疑難排解方法，例如，當發生不正確 IDL、C 或 C 預處理器語法時，或 MIDL 命令列上的偽 D 值導致 MIDL 報告難懂錯誤時。
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL 編譯器 MIDL，儲存預處理器輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372305"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="ebfb5-104">正在儲存預處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ebfb5-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="ebfb5-105">查看預處理器輸出可能是有效的疑難排解方法，例如，當發生不正確 IDL、C 或 C 預處理器語法時，或 MIDL 命令列上的偽 D 值導致 MIDL 報告難懂錯誤時。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="ebfb5-106">開發人員也可能想要檢查預處理器輸出，以判斷編譯器輸入資料流程中有哪些檔案和定義，例如必須解決類型重新定義衝突的困難案例。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="ebfb5-107">或者，某些開發人員可能會想要在預處理器上使用 [**/cpp \_ opt**](-cpp-opt.md)來強制執行私用參數，或可能想要查看切換開關的運作方式。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="ebfb5-108">從 MIDL 編譯執行取得前置處理過的檔案，最簡單且最不內斂的方式是使用 [**-savePP**](-savepp.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="ebfb5-109">**-SavePP** 參數只會防止 MIDL 刪除預處理器傳回 MIDL 的暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="ebfb5-110">請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="ebfb5-110">Consider the following:</span></span>

<span data-ttu-id="ebfb5-111">**midl-savePP-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1-Oicf-env win32 stub .idl**</span><span class="sxs-lookup"><span data-stu-id="ebfb5-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="ebfb5-112">這個指示詞會編譯 Stub，但仍會保留所有預處理器檔案。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="ebfb5-113">如果有) 以及每個匯入的檔案，MIDL 會為 IDL 和 ACF 檔案 (產生個別的預處理器執行。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="ebfb5-114">針對 DCOM 編譯，通常會產生數個預處理器檔案，即使 MIDL 以虛擬連續輸入資料流程的方式處理也是一樣。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="ebfb5-115">在一般的 Windows 程式設計環境中，可以在臨時目錄中找到暫存檔案，以作為檔案名，例如 \* MID。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="ebfb5-116">如果保留預處理器輸出，最好先監看 Temp 目錄中的最新檔案，以識別哪些檔案與預處理器執行相關聯。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="ebfb5-117">在簡單的情況下，例如編譯的 IDL 檔案不會直接或間接匯入其他檔案，或是在檢查最上層檔案時，可以直接叫用預處理器。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="ebfb5-118">直接執行 C/c + + 預處理器可能會顯示由 MIDL 遮罩或混淆的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="ebfb5-119">例如，下列兩個預處理器命令列可以用於前面加上引號的 MIDL 行：</span><span class="sxs-lookup"><span data-stu-id="ebfb5-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="ebfb5-120">**cl/E/nologo-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1 存根 .idl > stub. pp**</span><span class="sxs-lookup"><span data-stu-id="ebfb5-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="ebfb5-121">**cl/E/P-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1 stub**</span><span class="sxs-lookup"><span data-stu-id="ebfb5-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="ebfb5-122">在這兩個範例的第一個範例中， **/e** [**/nologo**](-nologo.md) 是 MIDL 叫用預處理器時新增的參數。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="ebfb5-123">預處理器輸出會傳送到 stdout (畫面) ，因此需要重新導向至檔案以進行檢查。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="ebfb5-124">在這些範例的第二個範例中， **/p** 會指示預處理器將輸出重新導向至檔案 \* 。在此情況下，會在目前的目錄中建立檔案。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="ebfb5-125">[**/Cpp \_ opt**](-cpp-opt.md)參數也可以用來取得前置處理過的檔案，但對於先前提及的方法而言很困難且較差。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="ebfb5-126">下列範例也會產生如先前範例所示的存根檔案。</span><span class="sxs-lookup"><span data-stu-id="ebfb5-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="ebfb5-127">下列範例中的引號是必要的：</span><span class="sxs-lookup"><span data-stu-id="ebfb5-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="ebfb5-128">**Midl-Oicf-win32-cpp \_ opt "/E/p-Id： \\ nt \\ public \\ sdk \\ inc.-DNTENV = 1" stub**</span><span class="sxs-lookup"><span data-stu-id="ebfb5-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




