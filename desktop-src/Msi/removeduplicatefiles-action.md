---
description: RemoveDuplicateFiles 動作會刪除 DuplicateFiles 動作所安裝的檔案。
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: RemoveDuplicateFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690239"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="d11ce-103">RemoveDuplicateFiles 動作</span><span class="sxs-lookup"><span data-stu-id="d11ce-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="d11ce-104">RemoveDuplicateFiles 動作會刪除 [DuplicateFiles](duplicatefiles-action.md) 動作所安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="d11ce-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d11ce-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="d11ce-105">Sequence Restrictions</span></span>

<span data-ttu-id="d11ce-106">RemoveDuplicateFiles 動作必須發生在 [InstallValidate](installvalidate-action.md) 動作之後，以及 [InstallFiles](installfiles-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="d11ce-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d11ce-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="d11ce-107">ActionData Messages</span></span>



| <span data-ttu-id="d11ce-108">欄位</span><span class="sxs-lookup"><span data-stu-id="d11ce-108">Field</span></span> | <span data-ttu-id="d11ce-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="d11ce-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="d11ce-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d11ce-110">\[1\]</span></span> | <span data-ttu-id="d11ce-111">已移除之檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d11ce-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="d11ce-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="d11ce-112">\[9\]</span></span> | <span data-ttu-id="d11ce-113">保存已移除檔案之目錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d11ce-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d11ce-114">備註</span><span class="sxs-lookup"><span data-stu-id="d11ce-114">Remarks</span></span>

<span data-ttu-id="d11ce-115">若要使用 RemoveDuplicateFiles 動作刪除以 [DuplicateFiles 動作](duplicatefiles-action.md) 複製的檔案，必須選取與 DuplicateFile 資料表中檔案的專案相關聯的元件才能移除。</span><span class="sxs-lookup"><span data-stu-id="d11ce-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="d11ce-116">使用 [DuplicateFile 資料表](duplicatefile-table.md) 的 DestFolder 資料行來指定屬性名稱，其值可識別目的資料夾。</span><span class="sxs-lookup"><span data-stu-id="d11ce-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



