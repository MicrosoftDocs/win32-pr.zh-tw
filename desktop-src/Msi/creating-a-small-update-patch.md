---
description: 建立 Windows Installer small update 的修補程式時，請遵循下列指導方針。
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: 建立小型更新修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999940"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="e73a4-103">建立小型更新修補程式</span><span class="sxs-lookup"><span data-stu-id="e73a4-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="e73a4-104">建立 [小型更新](small-updates.md)的修補程式時，作者應遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="e73a4-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="e73a4-105">小型更新修補程式必須針對單一的目標安裝設計。</span><span class="sxs-lookup"><span data-stu-id="e73a4-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="e73a4-106">小型更新修補程式應該使用最早的版本做為目標安裝。</span><span class="sxs-lookup"><span data-stu-id="e73a4-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="e73a4-107">小型更新修補程式應取代，並將任何先前的小型更新修補程式淘汰。</span><span class="sxs-lookup"><span data-stu-id="e73a4-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="e73a4-108">下列案例說明何時最適合小型更新修補程式。</span><span class="sxs-lookup"><span data-stu-id="e73a4-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="e73a4-109">您的公司發行了1.0 版的 Myproduct.msi。</span><span class="sxs-lookup"><span data-stu-id="e73a4-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="e73a4-110">不久之後，您就會針對名為 QFE1 的 Myproduct.msi 送出 [小型更新](small-updates.md) 修補程式。</span><span class="sxs-lookup"><span data-stu-id="e73a4-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="e73a4-111">這不會變更 [ [**ProductCode**](productcode.md) ] 屬性或 [**ProductVersion**](productversion.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e73a4-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="e73a4-112">稍後，您會撰寫 Myproduct.msi 的第二個 [小型更新](small-updates.md) 修補程式，稱為 QFE2。</span><span class="sxs-lookup"><span data-stu-id="e73a4-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="e73a4-113">第二個修補程式必須以 Myproduct.msi 版本1.0 為目標。</span><span class="sxs-lookup"><span data-stu-id="e73a4-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="e73a4-114">第二個修補程式不得以 Myproduct.msi 1.0 版和 Myproduct.msi 1.0 + QFE1 版本為目標。</span><span class="sxs-lookup"><span data-stu-id="e73a4-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="e73a4-115">套用 QFE2 時，應移除 QFE1。</span><span class="sxs-lookup"><span data-stu-id="e73a4-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



