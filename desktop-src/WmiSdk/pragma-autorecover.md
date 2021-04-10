---
description: 將 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma 自動回復
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944932"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="03338-103">pragma 自動回復</span><span class="sxs-lookup"><span data-stu-id="03338-103">pragma autorecover</span></span>

<span data-ttu-id="03338-104">**Pragma 自動** 復原預處理器命令會將 MOF 檔案新增至在存放庫復原期間所編譯的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="03338-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="03338-105">**自動** 回復 MOF 檔案的清單會儲存在此登錄機碼中：</span><span class="sxs-lookup"><span data-stu-id="03338-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="03338-106">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **自動回復 mof**</span><span class="sxs-lookup"><span data-stu-id="03338-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="03338-107">當作業系統啟動 WMI 時，WMI 會檢查 WMI 儲存機制的完整性。</span><span class="sxs-lookup"><span data-stu-id="03338-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="03338-108">如果存放庫損毀，WMI 就會自動重建存放庫，並在登錄中重新編譯此機碼中列出的任何 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="03338-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="03338-109">以下說明 pragma 自動回復命令的語法：</span><span class="sxs-lookup"><span data-stu-id="03338-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="03338-110">不過，使用此命令時，您必須遵守下列限制：</span><span class="sxs-lookup"><span data-stu-id="03338-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="03338-111">WMI 無法復原位於遠端電腦上的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="03338-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="03338-112">因此，此登錄機碼中列出的 MOF 檔案必須位於本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="03338-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="03338-113">當 WMI 復原 MOF 檔案時，您無法指定 MOF 編譯器所使用的命令列參數。</span><span class="sxs-lookup"><span data-stu-id="03338-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="03338-114">因此，您應該將 [pragma](-pragma.md) 命令納入不需要命令列切換的 MOF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="03338-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="03338-115">下列範例說明從這個登錄機碼復原 MOF 檔案時，WMI 未使用的一般命令列參數： **mofcomp.exe-N:Root \\ Test mymof. mof**</span><span class="sxs-lookup"><span data-stu-id="03338-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="03338-116">不過，您可以使用 MOF 檔案中的 [pragma](-pragma.md) 命令來指定命名空間。</span><span class="sxs-lookup"><span data-stu-id="03338-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="03338-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="03338-117">Requirements</span></span>



| <span data-ttu-id="03338-118">需求</span><span class="sxs-lookup"><span data-stu-id="03338-118">Requirement</span></span> | <span data-ttu-id="03338-119">值</span><span class="sxs-lookup"><span data-stu-id="03338-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="03338-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03338-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03338-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03338-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="03338-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03338-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03338-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03338-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03338-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03338-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03338-125">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="03338-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




