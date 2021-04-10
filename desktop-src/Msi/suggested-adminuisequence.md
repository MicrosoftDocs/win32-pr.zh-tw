---
description: Windows Installer 資料庫中的基本 AdminUISequence 資料表建議的動作順序。
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: 建議的 AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692376"
---
# <a name="suggested-adminuisequence"></a><span data-ttu-id="5e888-103">建議的 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="5e888-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="5e888-104">動作</span><span class="sxs-lookup"><span data-stu-id="5e888-104">Action</span></span>                                      | <span data-ttu-id="5e888-105">條件</span><span class="sxs-lookup"><span data-stu-id="5e888-105">Condition</span></span> | <span data-ttu-id="5e888-106">順序</span><span class="sxs-lookup"><span data-stu-id="5e888-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="5e888-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="5e888-108">-3</span><span class="sxs-lookup"><span data-stu-id="5e888-108">-3</span></span>       |
| <span data-ttu-id="5e888-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="5e888-110">-2</span><span class="sxs-lookup"><span data-stu-id="5e888-110">-2</span></span>       |
| <span data-ttu-id="5e888-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="5e888-112">-1</span><span class="sxs-lookup"><span data-stu-id="5e888-112">-1</span></span>       |
| <span data-ttu-id="5e888-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="5e888-114">140</span><span class="sxs-lookup"><span data-stu-id="5e888-114">140</span></span>      |
| [<span data-ttu-id="5e888-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="5e888-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="5e888-116">800</span><span class="sxs-lookup"><span data-stu-id="5e888-116">800</span></span>      |
| [<span data-ttu-id="5e888-117">FileCost</span><span class="sxs-lookup"><span data-stu-id="5e888-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="5e888-118">900</span><span class="sxs-lookup"><span data-stu-id="5e888-118">900</span></span>      |
| [<span data-ttu-id="5e888-119">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="5e888-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="5e888-120">1000</span><span class="sxs-lookup"><span data-stu-id="5e888-120">1000</span></span>     |
| <span data-ttu-id="5e888-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="5e888-122">1230</span><span class="sxs-lookup"><span data-stu-id="5e888-122">1230</span></span>     |
| <span data-ttu-id="5e888-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="5e888-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="5e888-124">1280</span><span class="sxs-lookup"><span data-stu-id="5e888-124">1280</span></span>     |
| [<span data-ttu-id="5e888-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="5e888-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="5e888-126">1300</span><span class="sxs-lookup"><span data-stu-id="5e888-126">1300</span></span>     |



 

 

 



