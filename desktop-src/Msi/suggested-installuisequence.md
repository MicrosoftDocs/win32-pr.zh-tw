---
description: Windows Installer 資料庫中的基本 InstalUISequence 資料表建議的動作順序。
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: 建議的 InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969400"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="88c42-103">建議的 InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="88c42-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="88c42-104">動作</span><span class="sxs-lookup"><span data-stu-id="88c42-104">Action</span></span>                                          | <span data-ttu-id="88c42-105">條件</span><span class="sxs-lookup"><span data-stu-id="88c42-105">Condition</span></span>                                                                                                  | <span data-ttu-id="88c42-106">順序</span><span class="sxs-lookup"><span data-stu-id="88c42-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="88c42-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="88c42-108">-3</span><span class="sxs-lookup"><span data-stu-id="88c42-108">-3</span></span>       |
| <span data-ttu-id="88c42-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="88c42-110">-2</span><span class="sxs-lookup"><span data-stu-id="88c42-110">-2</span></span>       |
| <span data-ttu-id="88c42-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="88c42-112">-1</span><span class="sxs-lookup"><span data-stu-id="88c42-112">-1</span></span>       |
| [<span data-ttu-id="88c42-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="88c42-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="88c42-114">100</span><span class="sxs-lookup"><span data-stu-id="88c42-114">100</span></span>      |
| <span data-ttu-id="88c42-115">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="88c42-116">140</span><span class="sxs-lookup"><span data-stu-id="88c42-116">140</span></span>      |
| [<span data-ttu-id="88c42-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="88c42-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="88c42-118">400</span><span class="sxs-lookup"><span data-stu-id="88c42-118">400</span></span>      |
| [<span data-ttu-id="88c42-119">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="88c42-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="88c42-120">未 [**安裝**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="88c42-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="88c42-121">500</span><span class="sxs-lookup"><span data-stu-id="88c42-121">500</span></span>      |
| [<span data-ttu-id="88c42-122">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="88c42-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="88c42-123">未 [**安裝**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="88c42-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="88c42-124">600</span><span class="sxs-lookup"><span data-stu-id="88c42-124">600</span></span>      |
| [<span data-ttu-id="88c42-125">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="88c42-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="88c42-126">800</span><span class="sxs-lookup"><span data-stu-id="88c42-126">800</span></span>      |
| [<span data-ttu-id="88c42-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="88c42-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="88c42-128">900</span><span class="sxs-lookup"><span data-stu-id="88c42-128">900</span></span>      |
| [<span data-ttu-id="88c42-129">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="88c42-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="88c42-130">1000</span><span class="sxs-lookup"><span data-stu-id="88c42-130">1000</span></span>     |
| <span data-ttu-id="88c42-131">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="88c42-132">未 [**安裝**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="88c42-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="88c42-133">1230</span><span class="sxs-lookup"><span data-stu-id="88c42-133">1230</span></span>     |
| <span data-ttu-id="88c42-134">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-134">ResumeDlg</span></span>                                       | <span data-ttu-id="88c42-135">[**已安裝**](installed.md) 和 ( [**繼續**](resume.md) 或 [**預先**](preselected.md) 選取) </span><span class="sxs-lookup"><span data-stu-id="88c42-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="88c42-136">1240</span><span class="sxs-lookup"><span data-stu-id="88c42-136">1240</span></span>     |
| <span data-ttu-id="88c42-137">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="88c42-138">[**已安裝**](installed.md)且不會 [**繼續**](resume.md)，也不會 [**預先**](preselected.md)選取</span><span class="sxs-lookup"><span data-stu-id="88c42-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="88c42-139">1250</span><span class="sxs-lookup"><span data-stu-id="88c42-139">1250</span></span>     |
| <span data-ttu-id="88c42-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="88c42-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="88c42-141">1280</span><span class="sxs-lookup"><span data-stu-id="88c42-141">1280</span></span>     |
| [<span data-ttu-id="88c42-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="88c42-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="88c42-143">1300</span><span class="sxs-lookup"><span data-stu-id="88c42-143">1300</span></span>     |



 

 

 



