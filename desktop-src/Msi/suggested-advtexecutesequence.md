---
description: Windows Installer 資料庫中的基本 AdvtExecuteSequence 資料表建議的動作順序。
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: 建議的 AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997286"
---
# <a name="suggested-advtexecutesequence"></a><span data-ttu-id="192d0-103">建議的 AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="192d0-103">Suggested AdvtExecuteSequence</span></span>



| <span data-ttu-id="192d0-104">動作</span><span class="sxs-lookup"><span data-stu-id="192d0-104">Action</span></span>                                                    | <span data-ttu-id="192d0-105">條件</span><span class="sxs-lookup"><span data-stu-id="192d0-105">Condition</span></span> | <span data-ttu-id="192d0-106">順序</span><span class="sxs-lookup"><span data-stu-id="192d0-106">Sequence</span></span> |
|-----------------------------------------------------------|-----------|----------|
| [<span data-ttu-id="192d0-107">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="192d0-107">CostInitialize</span></span>](costinitialize-action.md)               |           | <span data-ttu-id="192d0-108">800</span><span class="sxs-lookup"><span data-stu-id="192d0-108">800</span></span>      |
| [<span data-ttu-id="192d0-109">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="192d0-109">CostFinalize</span></span>](costfinalize-action.md)                   |           | <span data-ttu-id="192d0-110">1000</span><span class="sxs-lookup"><span data-stu-id="192d0-110">1000</span></span>     |
| [<span data-ttu-id="192d0-111">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="192d0-111">InstallValidate</span></span>](installvalidate-action.md)             |           | <span data-ttu-id="192d0-112">1400</span><span class="sxs-lookup"><span data-stu-id="192d0-112">1400</span></span>     |
| [<span data-ttu-id="192d0-113">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="192d0-113">InstallInitialize</span></span>](installinitialize-action.md)         |           | <span data-ttu-id="192d0-114">1500</span><span class="sxs-lookup"><span data-stu-id="192d0-114">1500</span></span>     |
| [<span data-ttu-id="192d0-115">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="192d0-115">CreateShortcuts</span></span>](createshortcuts-action.md)             |           | <span data-ttu-id="192d0-116">4500</span><span class="sxs-lookup"><span data-stu-id="192d0-116">4500</span></span>     |
| [<span data-ttu-id="192d0-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="192d0-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)         |           | <span data-ttu-id="192d0-118">4600</span><span class="sxs-lookup"><span data-stu-id="192d0-118">4600</span></span>     |
| [<span data-ttu-id="192d0-119">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="192d0-119">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md) |           | <span data-ttu-id="192d0-120">4700</span><span class="sxs-lookup"><span data-stu-id="192d0-120">4700</span></span>     |
| [<span data-ttu-id="192d0-121">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="192d0-121">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)       |           | <span data-ttu-id="192d0-122">4800</span><span class="sxs-lookup"><span data-stu-id="192d0-122">4800</span></span>     |
| [<span data-ttu-id="192d0-123">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="192d0-123">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)           |           | <span data-ttu-id="192d0-124">4900</span><span class="sxs-lookup"><span data-stu-id="192d0-124">4900</span></span>     |
| [<span data-ttu-id="192d0-125">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="192d0-125">PublishComponents</span></span>](publishcomponents-action.md)         |           | <span data-ttu-id="192d0-126">6200</span><span class="sxs-lookup"><span data-stu-id="192d0-126">6200</span></span>     |
| [<span data-ttu-id="192d0-127">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="192d0-127">PublishFeatures</span></span>](publishfeatures-action.md)             |           | <span data-ttu-id="192d0-128">6300</span><span class="sxs-lookup"><span data-stu-id="192d0-128">6300</span></span>     |
| [<span data-ttu-id="192d0-129">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="192d0-129">PublishProduct</span></span>](publishproduct-action.md)               |           | <span data-ttu-id="192d0-130">6400</span><span class="sxs-lookup"><span data-stu-id="192d0-130">6400</span></span>     |
| [<span data-ttu-id="192d0-131">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="192d0-131">InstallFinalize</span></span>](installfinalize-action.md)             |           | <span data-ttu-id="192d0-132">6600</span><span class="sxs-lookup"><span data-stu-id="192d0-132">6600</span></span>     |



 

 

 



