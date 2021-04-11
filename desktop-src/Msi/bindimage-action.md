---
description: BindImage 動作會系結必須系結至它所匯入之 Dll 的每個可執行檔或 DLL。
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: BindImage 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848951"
---
# <a name="bindimage-action"></a><span data-ttu-id="18106-103">BindImage 動作</span><span class="sxs-lookup"><span data-stu-id="18106-103">BindImage Action</span></span>

<span data-ttu-id="18106-104">BindImage 動作會系結必須系結至它所匯入之 Dll 的每個可執行檔或 DLL。</span><span class="sxs-lookup"><span data-stu-id="18106-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="18106-105">BindImage 動作會在 [BindImage](bindimage-table.md) 資料表中的每個檔案上運作，但僅適用于要在本機安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="18106-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="18106-106">安裝程式會計算從所有 Dll 匯入之每個函式的虛擬位址，然後將計算出的虛擬位址儲存在匯入映射的匯 [*入位址表*](i-gly.md) 中 (IAT) 。</span><span class="sxs-lookup"><span data-stu-id="18106-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="18106-107">BindImage 動作會在內部呼叫 **BindImageEx** Windows API。</span><span class="sxs-lookup"><span data-stu-id="18106-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="18106-108">順序限制</span><span class="sxs-lookup"><span data-stu-id="18106-108">Sequence Restrictions</span></span>

<span data-ttu-id="18106-109">BindImage 動作必須晚于 [InstallFiles](installfiles-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="18106-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="18106-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="18106-110">ActionData Messages</span></span>



| <span data-ttu-id="18106-111">欄位</span><span class="sxs-lookup"><span data-stu-id="18106-111">Field</span></span> | <span data-ttu-id="18106-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="18106-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="18106-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="18106-113">\[1\]</span></span> | <span data-ttu-id="18106-114">可執行檔的檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="18106-114">File identifier of executable.</span></span> |



 

 

 



