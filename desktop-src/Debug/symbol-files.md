---
description: 一般情況下，偵錯工具的資訊會儲存在與可執行檔分開的符號檔中。
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: 符號檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110204"
---
# <a name="symbol-files"></a><span data-ttu-id="7ac95-103">符號檔</span><span class="sxs-lookup"><span data-stu-id="7ac95-103">Symbol Files</span></span>

<span data-ttu-id="7ac95-104">一般情況下，偵錯工具的資訊會儲存在與可執行檔分開的符號檔中。</span><span class="sxs-lookup"><span data-stu-id="7ac95-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="7ac95-105">這項偵錯工具資訊的執行已經過多年的改變，而下列檔將提供有關這些各種不同實施的指引。</span><span class="sxs-lookup"><span data-stu-id="7ac95-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="7ac95-106">PDB 檔案</span><span class="sxs-lookup"><span data-stu-id="7ac95-106">PDB files</span></span>

<span data-ttu-id="7ac95-107">所有新式版本的 Microsoft 編譯器都會將編譯的可執行檔的偵錯工具儲存在個別的 *程式資料庫* 中， ( .pdb) 檔。</span><span class="sxs-lookup"><span data-stu-id="7ac95-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="7ac95-108">這個檔案通常稱為 *PDB*。</span><span class="sxs-lookup"><span data-stu-id="7ac95-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="7ac95-109">資料會儲存在可執行檔的個別檔案中，以協助限制可執行檔的大小、節省磁片儲存空間，並減少載入資料所需的時間。</span><span class="sxs-lookup"><span data-stu-id="7ac95-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="7ac95-110">這種方法也可以散發可執行檔，而不需要洩漏這項重要資訊，讓程式更容易進行反向工程。</span><span class="sxs-lookup"><span data-stu-id="7ac95-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="7ac95-111">若要建立 PDB，請根據您的組建工具的指示，建立您的可執行檔以及偵錯工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ac95-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="7ac95-112">DbgHelp API 可以使用 Pdb 來取得下列資訊。</span><span class="sxs-lookup"><span data-stu-id="7ac95-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="7ac95-113">publics 和匯出</span><span class="sxs-lookup"><span data-stu-id="7ac95-113">publics and exports</span></span>
-   <span data-ttu-id="7ac95-114">全域符號</span><span class="sxs-lookup"><span data-stu-id="7ac95-114">global symbols</span></span>
-   <span data-ttu-id="7ac95-115">本機符號</span><span class="sxs-lookup"><span data-stu-id="7ac95-115">local symbols</span></span>
-   <span data-ttu-id="7ac95-116">型別資料</span><span class="sxs-lookup"><span data-stu-id="7ac95-116">type data</span></span>
-   <span data-ttu-id="7ac95-117">原始程式檔</span><span class="sxs-lookup"><span data-stu-id="7ac95-117">source files</span></span>
-   <span data-ttu-id="7ac95-118">行號</span><span class="sxs-lookup"><span data-stu-id="7ac95-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="7ac95-119">DBG 檔案和內嵌的調試資訊</span><span class="sxs-lookup"><span data-stu-id="7ac95-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="7ac95-120">舊版的 Microsoft 工具組是用來將偵錯工具內嵌到可執行檔中，但通常會將它從副檔名為 dbg 的個別檔案中移除。</span><span class="sxs-lookup"><span data-stu-id="7ac95-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="7ac95-121">這通常稱為 *DBG* 檔案。</span><span class="sxs-lookup"><span data-stu-id="7ac95-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="7ac95-122">DBG 檔案使用的 PE 檔案格式與可執行檔相同。</span><span class="sxs-lookup"><span data-stu-id="7ac95-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="7ac95-123">DBGs 和內嵌偵錯工具的 DbgHelp API 支援受到限制，並且包含下列內容。</span><span class="sxs-lookup"><span data-stu-id="7ac95-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="7ac95-124">publics 和匯出</span><span class="sxs-lookup"><span data-stu-id="7ac95-124">publics and exports</span></span>
-   <span data-ttu-id="7ac95-125">全域符號</span><span class="sxs-lookup"><span data-stu-id="7ac95-125">global symbols</span></span>

 

 



