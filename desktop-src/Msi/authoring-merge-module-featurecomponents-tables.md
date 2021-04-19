---
description: 每個合併模組中都需要空白的 FeatureComponents 資料表。 如果目標 .msi 檔案沒有自己的 FeatureComponents 資料表，則此空白資料表會提供合併工具的架構。
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: 撰寫合併模組 FeatureComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976848"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a><span data-ttu-id="046ee-104">撰寫合併模組 FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="046ee-104">Authoring Merge Module FeatureComponents Tables</span></span>

<span data-ttu-id="046ee-105">每個合併模組中都需要空白的 [FeatureComponents 資料表](featurecomponents-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="046ee-105">A blank [FeatureComponents table](featurecomponents-table.md) is required in every merge module.</span></span> <span data-ttu-id="046ee-106">如果目標 .msi 檔案沒有自己的 FeatureComponents 資料表，則此空白資料表會提供合併工具的架構。</span><span class="sxs-lookup"><span data-stu-id="046ee-106">This empty table provides a schema for the merge tool if the target .msi file does not have its own FeatureComponents table.</span></span>

<span data-ttu-id="046ee-107">如果為，而且只有在，目標 .msi 檔案中沒有 FeatureComponents 資料表時，合併工具會使用模組中提供的空白資料表。</span><span class="sxs-lookup"><span data-stu-id="046ee-107">If, and only if, there is no FeatureComponents table in the target .msi file does the merge tool use the blank table provided in the module.</span></span> <span data-ttu-id="046ee-108">在此情況下，合併工具會在目標 .msi 檔案中建立重複的資料表，並將合併模組中的新元件與應用程式安裝套件中的功能建立關聯的資料列。</span><span class="sxs-lookup"><span data-stu-id="046ee-108">In this case, the merge tool creates a duplicate table in the target .msi file and adds rows that associate the new components in the merge module to the features in the application's installation package.</span></span>

 

 



