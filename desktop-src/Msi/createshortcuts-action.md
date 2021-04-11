---
description: CreateShortcuts 動作會管理快速鍵的建立。
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: CreateShortcuts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027330"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="e01c0-103">CreateShortcuts 動作</span><span class="sxs-lookup"><span data-stu-id="e01c0-103">CreateShortcuts Action</span></span>

<span data-ttu-id="e01c0-104">CreateShortcuts 動作會管理快速鍵的建立。</span><span class="sxs-lookup"><span data-stu-id="e01c0-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e01c0-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="e01c0-105">Sequence Restrictions</span></span>

<span data-ttu-id="e01c0-106">CreateShortcuts 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [RemoveShortcuts](removeshortcuts-action.md) 動作之後。</span><span class="sxs-lookup"><span data-stu-id="e01c0-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e01c0-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="e01c0-107">ActionData Messages</span></span>



| <span data-ttu-id="e01c0-108">欄位</span><span class="sxs-lookup"><span data-stu-id="e01c0-108">Field</span></span> | <span data-ttu-id="e01c0-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="e01c0-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="e01c0-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e01c0-110">\[1\]</span></span> | <span data-ttu-id="e01c0-111">已建立快捷方式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e01c0-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e01c0-112">備註</span><span class="sxs-lookup"><span data-stu-id="e01c0-112">Remarks</span></span>

<span data-ttu-id="e01c0-113">[CreateShortcuts] 動作會建立所選功能元件之主要檔案的快捷方式，以供安裝或廣告之用。</span><span class="sxs-lookup"><span data-stu-id="e01c0-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e01c0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e01c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e01c0-115">快速鍵資料表</span><span class="sxs-lookup"><span data-stu-id="e01c0-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="e01c0-116">MsiShortcutProperty 資料表</span><span class="sxs-lookup"><span data-stu-id="e01c0-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



