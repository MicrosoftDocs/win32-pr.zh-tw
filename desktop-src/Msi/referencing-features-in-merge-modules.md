---
description: 合併模組只會操作元件，而不會使用功能。 不過，合併模組中的某些資料表（例如 PublishComponent 資料表）包含參考特徵的欄位。
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: 參考合併模組中的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944154"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="68b72-104">參考合併模組中的功能</span><span class="sxs-lookup"><span data-stu-id="68b72-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="68b72-105">合併模組只會操作元件，而不會使用功能。</span><span class="sxs-lookup"><span data-stu-id="68b72-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="68b72-106">不過，合併模組中的某些資料表（例如 [PublishComponent 資料表](publishcomponent-table.md)）包含參考特徵的欄位。</span><span class="sxs-lookup"><span data-stu-id="68b72-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="68b72-107">Null GUID： {00000000-0000-0000-0000-000000000000} 必須撰寫到參考功能之 merge module 資料庫的任何欄位中。</span><span class="sxs-lookup"><span data-stu-id="68b72-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="68b72-108">合併模組合併為安裝套件時，合併工具會將 null GUID 取代為安裝套件中指定的功能，但需要特殊處理的資料表除外，例如 [ModuleSignature 資料表](modulesignature-table.md) 和 ModuleSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="68b72-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="68b72-109">請注意，如果使用 null GUID 做為主鍵，則不保證合併工具所取代的值是唯一的。</span><span class="sxs-lookup"><span data-stu-id="68b72-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="68b72-110">合併模組的作者負責確保當合併工具將 null Guid 取代為功能時，不會複製使用者介面中現有的主鍵。</span><span class="sxs-lookup"><span data-stu-id="68b72-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



