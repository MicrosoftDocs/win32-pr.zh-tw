---
title: 叫用 MIDL 編譯器
description: MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。 請參閱/target 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL 編譯器 MIDL，叫用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "106976329"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="a81a8-105">叫用 MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="a81a8-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="a81a8-106">MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="a81a8-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="a81a8-107">請參閱 [**/target**](-target.md) 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a81a8-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="a81a8-108">使用下列命令，從命令列執行 MIDL 編譯器：</span><span class="sxs-lookup"><span data-stu-id="a81a8-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="a81a8-109">**midl** *< 選項 >* **filename .idl**</span><span class="sxs-lookup"><span data-stu-id="a81a8-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="a81a8-110">其中 *< 選項 >* 代表您要使用的命令列選項，而 Filename 則是要編譯之 MIDL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a81a8-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="a81a8-111">當您使用 MIDL 編譯器 [**/help**](-help-.md) 和/？時，可使用 midl 編譯器參數和選項的完整清單。</span><span class="sxs-lookup"><span data-stu-id="a81a8-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="a81a8-112">開關。</span><span class="sxs-lookup"><span data-stu-id="a81a8-112">switches.</span></span> <span data-ttu-id="a81a8-113">這些參數是依類別目錄組織。</span><span class="sxs-lookup"><span data-stu-id="a81a8-113">The switches are organized by categories.</span></span> <span data-ttu-id="a81a8-114">如需詳細資訊，請參閱 [MIDL Command-Line 參考](midl-command-line-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="a81a8-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a81a8-115">新的 global 旗標 **$ (MIDL \_ 優化)** 存在於 win32 中。</span><span class="sxs-lookup"><span data-stu-id="a81a8-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="a81a8-116">使用此旗標編譯 .idl 檔案時，產生的存根可以利用指定平臺上可用的最新 RPC 功能，並可能改善應用程式的效能和穩定性。</span><span class="sxs-lookup"><span data-stu-id="a81a8-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="a81a8-117">使用 MIDL 時，建議應用程式使用這個旗標。</span><span class="sxs-lookup"><span data-stu-id="a81a8-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="a81a8-118">**midl** **$ (midl \_ 優化)** **...**</span><span class="sxs-lookup"><span data-stu-id="a81a8-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>