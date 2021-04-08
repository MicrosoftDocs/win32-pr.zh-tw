---
description: MsiUnpublishAssemblies 動作會管理要移除之 common language runtime 元件和 Win32 元件的公告。
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: MsiUnpublishAssemblies 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851352"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="cf7c9-103">MsiUnpublishAssemblies 動作</span><span class="sxs-lookup"><span data-stu-id="cf7c9-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="cf7c9-104">MsiUnpublishAssemblies 動作會管理要移除之 common language runtime 元件和 Win32 元件的公告。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="cf7c9-105">此動作會查詢 [MsiAssembly 資料表](msiassembly-table.md) ，以判斷哪些元件已從全域組件快取中移除已公告或已安裝的功能，以及哪些元件具有已公告或已安裝的父元件，從特定應用程式隔離的位置移除。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="cf7c9-106">如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="cf7c9-107">在執行 Windows XP 及更新版本的系統上，Windows Installer 可以安裝 Win32 元件作為 [並存元件](side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="cf7c9-108">如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cf7c9-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="cf7c9-109">Sequence Restrictions</span></span>

<span data-ttu-id="cf7c9-110">MsiUnpublishAssemblies 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的[InstallInitialize 動作](installinitialize-action.md)之後。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cf7c9-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="cf7c9-111">ActionData Messages</span></span>



| <span data-ttu-id="cf7c9-112">欄位</span><span class="sxs-lookup"><span data-stu-id="cf7c9-112">Field</span></span> | <span data-ttu-id="cf7c9-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="cf7c9-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="cf7c9-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cf7c9-114">\[1\]</span></span> | <span data-ttu-id="cf7c9-115">應用程式內容。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-115">Application context.</span></span>       |
| <span data-ttu-id="cf7c9-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="cf7c9-116">\[2\]</span></span> | <span data-ttu-id="cf7c9-117">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="cf7c9-118">備註</span><span class="sxs-lookup"><span data-stu-id="cf7c9-118">Remarks</span></span>

<span data-ttu-id="cf7c9-119">[MsiPublishAssemblies 動作](msipublishassemblies-action.md)會管理所通告或安裝之元件的公告。</span><span class="sxs-lookup"><span data-stu-id="cf7c9-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
