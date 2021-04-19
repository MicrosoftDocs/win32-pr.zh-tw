---
description: RemoveFiles 動作會移除 InstallFiles 動作先前安裝的檔案。
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: RemoveFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971491"
---
# <a name="removefiles-action"></a><span data-ttu-id="9c0a1-103">RemoveFiles 動作</span><span class="sxs-lookup"><span data-stu-id="9c0a1-103">RemoveFiles Action</span></span>

<span data-ttu-id="9c0a1-104">RemoveFiles 動作會移除 [InstallFiles](installfiles-action.md) 動作先前安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="9c0a1-105">這些檔案中的每一個都是由 [元件](component-table.md) 表格中專案的連結所管制。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="9c0a1-106">只有當元件安裝在本機時，具有元件的檔案才會解析為 *msiInstallStateAbsent* 狀態或 *msiInstallStateLocal* 狀態。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9c0a1-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="9c0a1-107">Sequence Restrictions</span></span>

<span data-ttu-id="9c0a1-108">呼叫 RemoveFiles 之前，必須先呼叫 [InstallValidate](installvalidate-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="9c0a1-109">如果使用 [InstallFiles](installfiles-action.md) 動作，它必須出現在 RemoveFiles 之後。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9c0a1-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="9c0a1-110">ActionData Messages</span></span>



| <span data-ttu-id="9c0a1-111">欄位</span><span class="sxs-lookup"><span data-stu-id="9c0a1-111">Field</span></span> | <span data-ttu-id="9c0a1-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="9c0a1-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="9c0a1-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9c0a1-113">\[1\]</span></span> | <span data-ttu-id="9c0a1-114">已移除之檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="9c0a1-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="9c0a1-115">\[9\]</span></span> | <span data-ttu-id="9c0a1-116">保存已移除檔案之目錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c0a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="9c0a1-117">Remarks</span></span>

<span data-ttu-id="9c0a1-118">如果沒有其他要移除的檔案，則可以從安裝程式資料庫省略 [RemoveFile](removefile-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="9c0a1-119">RemoveFiles 動作也可以移除 InstallFiles 動作未安裝的作者指定檔案。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="9c0a1-120">這些檔案會在 [RemoveFile](removefile-table.md) 資料表中指定。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="9c0a1-121">這些檔案中的每一個都是由 [元件](component-table.md) 表格中專案的連結所管制。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="9c0a1-122">如果檔案存在於指定的目錄中，這些檔案的元件會解析為任何作用中的動作 (狀態，而不是在 Off 或 Null 狀態中，則會移除) 。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="9c0a1-123">第一次安裝連結元件時，會嘗試移除 RemoveFile 資料表中指定的檔案，在重新安裝期間，以及在移除連結元件時，也會發生此情況。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="9c0a1-124">RemoveFiles 動作也可以移除資料夾。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="9c0a1-125">如果 RemoveFile 資料表的 FileName 資料行中的值為 null，則會移除空的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="9c0a1-126">移除先前安裝的檔案時，RemoveFiles 動作會查詢與 [InstallFiles](installfiles-action.md) 動作所查詢之相同資料表中的相同欄位，但 RemoveFiles 動作未使用 [媒體資料表](media-table.md) 的例外。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="9c0a1-127">您可以在 RemoveFile 資料表的 FileName 資料行中，以當地語系化的文字指定目的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9c0a1-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



