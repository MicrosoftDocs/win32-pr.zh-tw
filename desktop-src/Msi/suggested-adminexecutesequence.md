---
description: Windows Installer 資料庫中的基本 AdminExecuteSequence 資料表建議的動作順序。
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: 建議的 AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ead890630b397062c6b8e645385b2810fa39d95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512012"
---
# <a name="suggested-adminexecutesequence"></a><span data-ttu-id="0c0d5-103">建議的 AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="0c0d5-103">Suggested AdminExecuteSequence</span></span>



| <span data-ttu-id="0c0d5-104">動作</span><span class="sxs-lookup"><span data-stu-id="0c0d5-104">Action</span></span>                                                | <span data-ttu-id="0c0d5-105">條件</span><span class="sxs-lookup"><span data-stu-id="0c0d5-105">Condition</span></span> | <span data-ttu-id="0c0d5-106">順序</span><span class="sxs-lookup"><span data-stu-id="0c0d5-106">Sequence</span></span> |
|-------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="0c0d5-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="0c0d5-107">CostInitialize</span></span>](costinitialize-action.md)           |           | <span data-ttu-id="0c0d5-108">800</span><span class="sxs-lookup"><span data-stu-id="0c0d5-108">800</span></span>      |
| [<span data-ttu-id="0c0d5-109">FileCost</span><span class="sxs-lookup"><span data-stu-id="0c0d5-109">FileCost</span></span>](filecost-action.md)                       |           | <span data-ttu-id="0c0d5-110">900</span><span class="sxs-lookup"><span data-stu-id="0c0d5-110">900</span></span>      |
| [<span data-ttu-id="0c0d5-111">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="0c0d5-111">CostFinalize</span></span>](costfinalize-action.md)               |           | <span data-ttu-id="0c0d5-112">1000</span><span class="sxs-lookup"><span data-stu-id="0c0d5-112">1000</span></span>     |
| [<span data-ttu-id="0c0d5-113">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="0c0d5-113">InstallValidate</span></span>](installvalidate-action.md)         |           | <span data-ttu-id="0c0d5-114">1400</span><span class="sxs-lookup"><span data-stu-id="0c0d5-114">1400</span></span>     |
| [<span data-ttu-id="0c0d5-115">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0c0d5-115">InstallInitialize</span></span>](installinitialize-action.md)     |           | <span data-ttu-id="0c0d5-116">1500</span><span class="sxs-lookup"><span data-stu-id="0c0d5-116">1500</span></span>     |
| [<span data-ttu-id="0c0d5-117">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="0c0d5-117">InstallAdminPackage</span></span>](installadminpackage-action.md) |           | <span data-ttu-id="0c0d5-118">3900</span><span class="sxs-lookup"><span data-stu-id="0c0d5-118">3900</span></span>     |
| [<span data-ttu-id="0c0d5-119">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="0c0d5-119">InstallFiles</span></span>](installfiles-action.md)               |           | <span data-ttu-id="0c0d5-120">4000</span><span class="sxs-lookup"><span data-stu-id="0c0d5-120">4000</span></span>     |
| [<span data-ttu-id="0c0d5-121">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="0c0d5-121">InstallFinalize</span></span>](installfinalize-action.md)         |           | <span data-ttu-id="0c0d5-122">6600</span><span class="sxs-lookup"><span data-stu-id="0c0d5-122">6600</span></span>     |



 

 

 



