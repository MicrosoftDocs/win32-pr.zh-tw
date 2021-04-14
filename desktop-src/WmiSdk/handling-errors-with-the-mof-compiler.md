---
description: 如果 MOF 編譯器無法完成 MOF 檔案的編譯，WMI 儲存機制可能會處於未定義狀態。
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: 使用 MOF 編譯器處理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469496"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="db682-103">使用 MOF 編譯器處理錯誤</span><span class="sxs-lookup"><span data-stu-id="db682-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="db682-104">如果 MOF 編譯器無法完成 MOF 檔案的編譯，WMI 儲存機制可能會處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="db682-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="db682-105">例如，如果您要編譯 MOF 檔案，且使用 **-class：以** 命令列參數，則編譯會在 MOF 檔案中指定的類別已存在時終止。</span><span class="sxs-lookup"><span data-stu-id="db682-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="db682-106">MOF 編譯器會將任何定義的類別或實例儲存在存放庫中，直到編譯器停止為止。</span><span class="sxs-lookup"><span data-stu-id="db682-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="db682-107">在某些情況下，這可能會讓 WMI 存放庫處於未定義的情況。</span><span class="sxs-lookup"><span data-stu-id="db682-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="db682-108">在這種情況下，您可能需要停止 WMI、刪除 WMI 儲存機制，並讓 WMI 重建它。</span><span class="sxs-lookup"><span data-stu-id="db682-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="db682-109">當 WMI 重新開機時，會重建包含 [**pragma 自動**](pragma-autorecover.md)回復 [預處理器命令](preprocessor-commands.md) 的所有 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="db682-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="db682-110">您必須手動重新編譯任何不包含語句的 MOF 檔案 `#pragma autorecover` 。</span><span class="sxs-lookup"><span data-stu-id="db682-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="db682-111">如需如何使用 MOF 語法宣告類別和實例的詳細資訊，請參閱 [設計受控物件格式 (mof) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="db682-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db682-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="db682-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db682-113">編譯 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="db682-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="db682-114">**mofcomp.exe**</span><span class="sxs-lookup"><span data-stu-id="db682-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="db682-115">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="db682-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



