---
title: 新的檔案歷程記錄功能
description: 新的檔案歷程記錄功能
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104093428"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="7f65f-103">新的檔案歷程記錄功能</span><span class="sxs-lookup"><span data-stu-id="7f65f-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="7f65f-104">平台</span><span class="sxs-lookup"><span data-stu-id="7f65f-104">Platform</span></span>

<span data-ttu-id="7f65f-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f65f-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="7f65f-106">Description</span><span class="sxs-lookup"><span data-stu-id="7f65f-106">Description</span></span>

<span data-ttu-id="7f65f-107">新的檔案歷程記錄功能會取代現有的備份和還原功能，並為儲存在使用者程式庫中的使用者檔案提供保護。</span><span class="sxs-lookup"><span data-stu-id="7f65f-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="7f65f-108">提供一組 Api，可讓開發人員以程式設計方式啟用檔案歷程記錄並選取特定的儲存體目標。</span><span class="sxs-lookup"><span data-stu-id="7f65f-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="7f65f-109">您可以在 MSDN 上取得這些 Api 的檔。</span><span class="sxs-lookup"><span data-stu-id="7f65f-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="7f65f-110">這可能會影響與資料保護相關的工作流程，以及相依于 Windows 備份和還原功能的檔。</span><span class="sxs-lookup"><span data-stu-id="7f65f-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="7f65f-111">我們不建議同時使用這兩項功能。</span><span class="sxs-lookup"><span data-stu-id="7f65f-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="7f65f-112">檔案歷程記錄會檢查備份排程是否存在且是否為作用中，如果找到的話，就不會讓使用者開啟它。</span><span class="sxs-lookup"><span data-stu-id="7f65f-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="7f65f-113">在此情況下，想要使用檔案歷程記錄的使用者將必須刪除 Windows 備份排程。</span><span class="sxs-lookup"><span data-stu-id="7f65f-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7f65f-114">表現</span><span class="sxs-lookup"><span data-stu-id="7f65f-114">Manifestation</span></span>

<span data-ttu-id="7f65f-115">工作流程可能會中斷，而先前存取 Windows 備份和還原功能的方法的檔則需要更新，以反映這些變更。</span><span class="sxs-lookup"><span data-stu-id="7f65f-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="7f65f-116">解決方法</span><span class="sxs-lookup"><span data-stu-id="7f65f-116">Solution</span></span>

<span data-ttu-id="7f65f-117">修訂應用程式，其中包含會對新的檔案歷程記錄功能造成負面影響的工作流程，以移除任何衝突並併入新的 Api 集。</span><span class="sxs-lookup"><span data-stu-id="7f65f-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="7f65f-118">測試</span><span class="sxs-lookup"><span data-stu-id="7f65f-118">Tests</span></span>

<span data-ttu-id="7f65f-119">API 可讓開發人員判斷檔案歷程記錄是否已開啟。</span><span class="sxs-lookup"><span data-stu-id="7f65f-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




