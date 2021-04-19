---
description: CreateFolders 動作會針對已設定為要安裝的元件，建立空的資料夾。
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: CreateFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976588"
---
# <a name="createfolders-action"></a><span data-ttu-id="77609-103">CreateFolders 動作</span><span class="sxs-lookup"><span data-stu-id="77609-103">CreateFolders Action</span></span>

<span data-ttu-id="77609-104">CreateFolders 動作會針對已設定為要安裝的元件，建立空的資料夾。</span><span class="sxs-lookup"><span data-stu-id="77609-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="77609-105">安裝程式會針對在本機執行並從來源執行的元件建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="77609-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="77609-106">新建立的資料夾會以適當的元件識別碼進行註冊。</span><span class="sxs-lookup"><span data-stu-id="77609-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="77609-107">CreateFolders 動作會查詢 [CreateFolder 資料表](createfolder-table.md) 和 [元件資料表](component-table.md)。</span><span class="sxs-lookup"><span data-stu-id="77609-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="77609-108">順序限制</span><span class="sxs-lookup"><span data-stu-id="77609-108">Sequence Restrictions</span></span>

<span data-ttu-id="77609-109">CreateFolders 動作必須在 [InstallFiles](installfiles-action.md) 動作之前，或在將檔案新增至資料夾的任何動作之前執行。</span><span class="sxs-lookup"><span data-stu-id="77609-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="77609-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="77609-110">ActionData Messages</span></span>



| <span data-ttu-id="77609-111">欄位</span><span class="sxs-lookup"><span data-stu-id="77609-111">Field</span></span> | <span data-ttu-id="77609-112">動作資料描述的描述</span><span class="sxs-lookup"><span data-stu-id="77609-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="77609-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="77609-113">\[1\]</span></span> | <span data-ttu-id="77609-114">資料夾的目錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="77609-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="77609-115">備註</span><span class="sxs-lookup"><span data-stu-id="77609-115">Remarks</span></span>

<span data-ttu-id="77609-116">安裝程式不會在應用程式卸載期間自動移除 CreateFolders 動作所建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="77609-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="77609-117">只有在動作順序中包含 [RemoveFolders 動作](removefolders-action.md) 時，安裝程式才會移除資料夾。</span><span class="sxs-lookup"><span data-stu-id="77609-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



