---
description: 可以撰寫合併模組 ( .msm 檔案) ，以包含可由合併模組的取用者設定的屬性。
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: 可設定的合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980065"
---
# <a name="configurable-merge-modules"></a><span data-ttu-id="884d6-103">可設定的合併模組</span><span class="sxs-lookup"><span data-stu-id="884d6-103">Configurable Merge Modules</span></span>

<span data-ttu-id="884d6-104">可以撰寫合併模組 ( .msm 檔案) ，以包含可由合併模組的取用者設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="884d6-104">Merge modules (.msm files) may be authored to contain attributes that are configurable by the consumer of the merge module.</span></span> <span data-ttu-id="884d6-105">這可讓合併模組在安裝套件和模組與使用者合併及安裝時進行設定。</span><span class="sxs-lookup"><span data-stu-id="884d6-105">This enables the merge module to be configured at the time the installation package and module are merged and installed by the end-user.</span></span> <span data-ttu-id="884d6-106">可設定的合併模組需要 Mergemod.dll 2.0 版，但可以在任何版本的 Windows Installer 上執行。</span><span class="sxs-lookup"><span data-stu-id="884d6-106">Configurable merge modules require Mergemod.dll version 2.0 but can run on any version of the Windows Installer.</span></span>

<span data-ttu-id="884d6-107">可設定合併模組的執行是由兩個部分所組成。</span><span class="sxs-lookup"><span data-stu-id="884d6-107">The implementation of configurable merge modules consists of two parts.</span></span> <span data-ttu-id="884d6-108">首先，建立合併模組 ( .msm 檔) 時，合併模組作者會將資訊加入模組資料庫，以指定可修改哪些專案，以及模組使用者如何設定這些專案。</span><span class="sxs-lookup"><span data-stu-id="884d6-108">First, when creating the merge module (.msm file), the merge module author adds information to the module database that specifies which items can be modified and how these items can be configured by the module user.</span></span> <span data-ttu-id="884d6-109">作者將專案加入至[合併模組資料庫資料表](merge-module-database-tables.md)，這些資料表保留給可設定的資訊 ([ModuleConfiguration 資料表](moduleconfiguration-table.md)和[ModuleSubstitution 資料表](modulesubstitution-table.md)) 、更新[ \_ 驗證資料表](-validation-table.md)，以及將可設定合併模組資料表的專案加入至[ModuleIgnoreTable 資料表](moduleignoretable-table.md)。</span><span class="sxs-lookup"><span data-stu-id="884d6-109">The author adds entries to the [Merge Module Database Tables](merge-module-database-tables.md) that are reserved for configurable information ([ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md)), updates the [\_Validation table](-validation-table.md), and adds entries for the configurable merge module tables to the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span> <span data-ttu-id="884d6-110">ModuleIgnore 資料表的新增專案是使模組與2.0 之前的 Mergemod.dll 版本相容所需的專案。</span><span class="sxs-lookup"><span data-stu-id="884d6-110">The additions to the ModuleIgnore table are required to make the module compatible with Mergemod.dll versions earlier than 2.0.</span></span>

<span data-ttu-id="884d6-111">其次，將模組合併到安裝套件 ( .msi 檔案) 時，模組的使用者會使用合併工具。</span><span class="sxs-lookup"><span data-stu-id="884d6-111">Second, when merging the module into an installation package (.msi file), the end-user of the module uses a merge tool.</span></span> <span data-ttu-id="884d6-112">合併工具會呼叫 Mergemod.dll，以將模組中的設定資訊公開至用戶端設定工具。</span><span class="sxs-lookup"><span data-stu-id="884d6-112">The merge tool calls Mergemod.dll to expose the configuration information in the module to a client configuration tool.</span></span> <span data-ttu-id="884d6-113">設定工具可能與終端使用者互動，但不需要公開所有可能的設定選項。</span><span class="sxs-lookup"><span data-stu-id="884d6-113">The configuration tool may interact with the end-user but is not required to expose all possible configuration options.</span></span> <span data-ttu-id="884d6-114">如果使用者拒絕提供可設定專案的選取專案，模組可能會提供預設值。</span><span class="sxs-lookup"><span data-stu-id="884d6-114">If the user declines to provide a selection for a configurable item, the module may provide a default value.</span></span> <span data-ttu-id="884d6-115">當使用者提供設定工具的選取專案之後，合併工具就會呼叫 Mergemod.dll 來執行合併。</span><span class="sxs-lookup"><span data-stu-id="884d6-115">After the user gives the configuration tool his selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

<span data-ttu-id="884d6-116">可設定的合併模組與早于 Mergemod.dll 2.0 版的工具完全相容。</span><span class="sxs-lookup"><span data-stu-id="884d6-116">Configurable merge modules are fully compatible with tools earlier than Mergemod.dll version 2.0.</span></span> <span data-ttu-id="884d6-117">在這些情況下，工具會使用模組中的預設值。</span><span class="sxs-lookup"><span data-stu-id="884d6-117">In these cases, the tool uses the default values in the module.</span></span>

<span data-ttu-id="884d6-118">如需詳細資訊，請參閱 [使用可設定的合併模組](using-configurable-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="884d6-118">For more information, see [Using Configurable Merge Modules](using-configurable-merge-modules.md).</span></span>

 

 



