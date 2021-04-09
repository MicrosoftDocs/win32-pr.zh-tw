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
# <a name="suggested-adminuisequence"></a><span data-ttu-id="7d22c-103">建議的 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="7d22c-103">Suggested AdminUISequence</span></span>



| <span data-ttu-id="7d22c-104">動作</span><span class="sxs-lookup"><span data-stu-id="7d22c-104">Action</span></span>                                      | <span data-ttu-id="7d22c-105">條件</span><span class="sxs-lookup"><span data-stu-id="7d22c-105">Condition</span></span> | <span data-ttu-id="7d22c-106">順序</span><span class="sxs-lookup"><span data-stu-id="7d22c-106">Sequence</span></span> |
|---------------------------------------------|-----------|----------|
| <span data-ttu-id="7d22c-107">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-107">FatalErrorDlg</span></span>                               |           | <span data-ttu-id="7d22c-108">-3</span><span class="sxs-lookup"><span data-stu-id="7d22c-108">-3</span></span>       |
| <span data-ttu-id="7d22c-109">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-109">UserExitDlg</span></span>                                 |           | <span data-ttu-id="7d22c-110">-2</span><span class="sxs-lookup"><span data-stu-id="7d22c-110">-2</span></span>       |
| <span data-ttu-id="7d22c-111">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-111">ExitDlg</span></span>                                     |           | <span data-ttu-id="7d22c-112">-1</span><span class="sxs-lookup"><span data-stu-id="7d22c-112">-1</span></span>       |
| <span data-ttu-id="7d22c-113">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-113">PrepareDlg</span></span>                                  |           | <span data-ttu-id="7d22c-114">140</span><span class="sxs-lookup"><span data-stu-id="7d22c-114">140</span></span>      |
| [<span data-ttu-id="7d22c-115">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="7d22c-115">CostInitialize</span></span>](costinitialize-action.md) |           | <span data-ttu-id="7d22c-116">800</span><span class="sxs-lookup"><span data-stu-id="7d22c-116">800</span></span>      |
| [<span data-ttu-id="7d22c-117">FileCost</span><span class="sxs-lookup"><span data-stu-id="7d22c-117">FileCost</span></span>](filecost-action.md)             |           | <span data-ttu-id="7d22c-118">900</span><span class="sxs-lookup"><span data-stu-id="7d22c-118">900</span></span>      |
| [<span data-ttu-id="7d22c-119">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="7d22c-119">CostFinalize</span></span>](costfinalize-action.md)     |           | <span data-ttu-id="7d22c-120">1000</span><span class="sxs-lookup"><span data-stu-id="7d22c-120">1000</span></span>     |
| <span data-ttu-id="7d22c-121">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-121">AdminWelcomeDlg</span></span>                             |           | <span data-ttu-id="7d22c-122">1230</span><span class="sxs-lookup"><span data-stu-id="7d22c-122">1230</span></span>     |
| <span data-ttu-id="7d22c-123">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="7d22c-123">ProgressDlg</span></span>                                 |           | <span data-ttu-id="7d22c-124">1280</span><span class="sxs-lookup"><span data-stu-id="7d22c-124">1280</span></span>     |
| [<span data-ttu-id="7d22c-125">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="7d22c-125">ExecuteAction</span></span>](executeaction-action.md)   |           | <span data-ttu-id="7d22c-126">1300</span><span class="sxs-lookup"><span data-stu-id="7d22c-126">1300</span></span>     |



 

 

 



