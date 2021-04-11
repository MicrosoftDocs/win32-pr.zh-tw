---
description: 強烈建議您在第一次嘗試安裝封裝之前，先對每個新的或新修改的安裝套件執行驗證。
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: 套件驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848772"
---
# <a name="package-validation"></a><span data-ttu-id="6a426-103">套件驗證</span><span class="sxs-lookup"><span data-stu-id="6a426-103">Package Validation</span></span>

<span data-ttu-id="6a426-104">強烈建議您在第一次嘗試安裝封裝之前，先對每個新的或新修改的安裝套件執行驗證。</span><span class="sxs-lookup"><span data-stu-id="6a426-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="6a426-105">封裝驗證封裝含下列三個進程：</span><span class="sxs-lookup"><span data-stu-id="6a426-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="6a426-106">內部驗證</span><span class="sxs-lookup"><span data-stu-id="6a426-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="6a426-107">字串集區驗證</span><span class="sxs-lookup"><span data-stu-id="6a426-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="6a426-108">內部一致性評估工具-Ices-003</span><span class="sxs-lookup"><span data-stu-id="6a426-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="6a426-109">合併模組應使用 [驗證合併模組](validating-merge-modules.md)中描述的方法進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6a426-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="6a426-110">Evalcom2.dll 提供的 COM 物件可執行安裝封裝和合併模組的驗證作業。</span><span class="sxs-lookup"><span data-stu-id="6a426-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="6a426-111">主要物件會執行 C/c + + 程式的介面。</span><span class="sxs-lookup"><span data-stu-id="6a426-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="6a426-112">如需詳細資訊，請參閱 [驗證自動化](validation-automation.md)。</span><span class="sxs-lookup"><span data-stu-id="6a426-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



