---
description: 在編譯 MOF 檔案時，您有兩個選擇：使用命令列公用程式或使用程式設計介面。
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: 在檔案上執行 MOF 編譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230246"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="f90da-103">在檔案上執行 MOF 編譯器</span><span class="sxs-lookup"><span data-stu-id="f90da-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="f90da-104">在編譯 MOF 檔案時，您有兩個選擇：使用命令列公用程式或使用程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="f90da-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="f90da-105">在您執行 MOF 編譯器之前 [**Mofcomp.exe**](mofcomp.md)，未向 wmi 註冊提供者，且在 MOF 檔案中建立的類別在 [*wmi 存放庫*](gloss-w.md)中無法使用。</span><span class="sxs-lookup"><span data-stu-id="f90da-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="f90da-106">下列程式說明如何編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f90da-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="f90da-107">**從命令列執行 MOF 編譯器 on file**</span><span class="sxs-lookup"><span data-stu-id="f90da-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="f90da-108">使用下列語法，從命令列呼叫 MOF 編譯器。</span><span class="sxs-lookup"><span data-stu-id="f90da-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="f90da-109">**Mofcomp.exe** _MOFfile_ \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f90da-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="f90da-110">MOF 編譯器支援各種不同的參數來控制特殊的處理情況。</span><span class="sxs-lookup"><span data-stu-id="f90da-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="f90da-111">所有參數都是選擇性的，且允許任何參數組合。</span><span class="sxs-lookup"><span data-stu-id="f90da-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="f90da-112">不過，將某些參數與其他參數搭配使用並不合理。</span><span class="sxs-lookup"><span data-stu-id="f90da-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="f90da-113">例如，若要結合 **-class： updateonly** 和 **-class：以** 參數會導致編譯器無法執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="f90da-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="f90da-114">根據預設，Mofcomp.exe 會將編譯的類別儲存在根 \\ 預設 WMI 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="f90da-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="f90da-115">請注意，Mofcomp.exe 的預設命名空間與腳本的預設命名空間不同。</span><span class="sxs-lookup"><span data-stu-id="f90da-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="f90da-116">腳本的預設命名空間是在 [Advanced （Advanced）] 索引標籤的 WMI 控制項中指定的。如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="f90da-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="f90da-117">您可以透過兩種方式來變更接收類別的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f90da-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="f90da-118">針對 **mofcomp.exe** 命令使用 **-N** 參數。</span><span class="sxs-lookup"><span data-stu-id="f90da-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="f90da-119">在 MOF 檔案中插入預處理器命令 \# [**pragma 命名空間**](pragma-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="f90da-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="f90da-120">（選擇性）您可以用程式設計的方式編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f90da-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="f90da-121">如需詳細資訊，請參閱 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)。</span><span class="sxs-lookup"><span data-stu-id="f90da-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f90da-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="f90da-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f90da-123">編譯 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="f90da-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="f90da-124">**mofcomp.exe**</span><span class="sxs-lookup"><span data-stu-id="f90da-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="f90da-125">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="f90da-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



