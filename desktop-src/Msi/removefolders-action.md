---
description: RemoveFolders 動作會移除任何連結至元件的資料夾，這些資料夾已設定為要從來源移除或執行。 只有當這些資料夾是空的時，才會移除這些資料夾。 如果移除資料夾，則會以適當的元件識別碼取消註冊。
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: RemoveFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193679"
---
# <a name="removefolders-action"></a><span data-ttu-id="c6d99-105">RemoveFolders 動作</span><span class="sxs-lookup"><span data-stu-id="c6d99-105">RemoveFolders Action</span></span>

<span data-ttu-id="c6d99-106">RemoveFolders 動作會移除任何連結至元件的資料夾，這些資料夾已設定為要從來源移除或執行。</span><span class="sxs-lookup"><span data-stu-id="c6d99-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="c6d99-107">只有當這些資料夾是空的時，才會移除這些資料夾。</span><span class="sxs-lookup"><span data-stu-id="c6d99-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="c6d99-108">如果移除資料夾，則會以適當的元件識別碼取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c6d99-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c6d99-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="c6d99-109">Sequence Restrictions</span></span>

<span data-ttu-id="c6d99-110">RemoveFolders 動作必須在 [RemoveFiles](removefiles-action.md) 動作之後，或可能會從資料夾移除檔案的任何動作。</span><span class="sxs-lookup"><span data-stu-id="c6d99-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c6d99-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="c6d99-111">ActionData Messages</span></span>



| <span data-ttu-id="c6d99-112">欄位</span><span class="sxs-lookup"><span data-stu-id="c6d99-112">Field</span></span> | <span data-ttu-id="c6d99-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="c6d99-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="c6d99-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c6d99-114">\[1\]</span></span> | <span data-ttu-id="c6d99-115">已移除資料夾的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6d99-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6d99-116">備註</span><span class="sxs-lookup"><span data-stu-id="c6d99-116">Remarks</span></span>

<span data-ttu-id="c6d99-117">安裝程式在卸載應用程式期間，不會自動移除 [CreateFolders 動作](createfolders-action.md) 所建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c6d99-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="c6d99-118">您必須將 RemoveFolders 動作撰寫至動作順序，指示安裝程式移除這些資料夾。</span><span class="sxs-lookup"><span data-stu-id="c6d99-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="c6d99-119">若要指定資料夾的名稱和位置，請使用 CreateFolder 資料表的 [目錄] 資料 \_ 行。 [](createfolder-table.md)</span><span class="sxs-lookup"><span data-stu-id="c6d99-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="c6d99-120">CreateFolder 資料表中的每個資料夾名稱都假設為定義資料夾位置的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6d99-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="c6d99-121">若要指定擁有資料夾的元件，請使用 [元件資料表](component-table.md)的 [元件] 資料行。</span><span class="sxs-lookup"><span data-stu-id="c6d99-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



