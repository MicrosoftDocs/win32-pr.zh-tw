---
description: MsiPublishAssemblies 動作會管理 common language runtime 元件和 Win32 元件的公告。
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: MsiPublishAssemblies 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979399"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="e8f21-103">MsiPublishAssemblies 動作</span><span class="sxs-lookup"><span data-stu-id="e8f21-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="e8f21-104">MsiPublishAssemblies 動作會管理 common language runtime 元件和 Win32 元件的公告。</span><span class="sxs-lookup"><span data-stu-id="e8f21-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="e8f21-105">此動作會查詢 [MsiAssembly 資料表](msiassembly-table.md) ，以判斷哪些元件具有要在全域組件快取中通告或安裝的功能，以及哪些元件有父元件要被通告或安裝到特定應用程式的隔離位置。</span><span class="sxs-lookup"><span data-stu-id="e8f21-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="e8f21-106">如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f21-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="e8f21-107">在 Microsoft Windows XP 及更新版本的系統上，Windows Installer 可以安裝 Win32 元件作為 [並存元件](side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f21-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="e8f21-108">如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f21-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e8f21-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="e8f21-109">Sequence Restrictions</span></span>

<span data-ttu-id="e8f21-110">MsiPublishAssemblies 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)或[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中的[InstallInitialize 動作](installinitialize-action.md)之後。</span><span class="sxs-lookup"><span data-stu-id="e8f21-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e8f21-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="e8f21-111">ActionData Messages</span></span>



| <span data-ttu-id="e8f21-112">欄位</span><span class="sxs-lookup"><span data-stu-id="e8f21-112">Field</span></span> | <span data-ttu-id="e8f21-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="e8f21-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="e8f21-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e8f21-114">\[1\]</span></span> | <span data-ttu-id="e8f21-115">應用程式內容。</span><span class="sxs-lookup"><span data-stu-id="e8f21-115">Application context.</span></span>       |
| <span data-ttu-id="e8f21-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e8f21-116">\[2\]</span></span> | <span data-ttu-id="e8f21-117">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f21-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="e8f21-118">備註</span><span class="sxs-lookup"><span data-stu-id="e8f21-118">Remarks</span></span>

<span data-ttu-id="e8f21-119">如需詳細資訊，請參閱 [元件](assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="e8f21-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="e8f21-120">[MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md)會管理要移除之元件的公告。</span><span class="sxs-lookup"><span data-stu-id="e8f21-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
