---
title: 使用 AccChecker 進行測試
description: 描述合併 AccChecker 的一般測試工作流程。
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- 使用 AccChecker 進行測試
- AccChecker，測試工作流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507072"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="e370d-105">使用 AccChecker 進行測試</span><span class="sxs-lookup"><span data-stu-id="e370d-105">Testing with AccChecker</span></span>

<span data-ttu-id="e370d-106">下列案例描述當您使用 AccChecker 進行測試時，通常會遵循的步驟。</span><span class="sxs-lookup"><span data-stu-id="e370d-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="e370d-107">當 AccChecker 驗證常式正在執行時，與主機電腦的使用者互動可能會干擾某些常式。</span><span class="sxs-lookup"><span data-stu-id="e370d-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="e370d-108">我們建議您在 AccChecker 通知使用者所有工作都已完成之前，不會進行進一步的使用者互動。</span><span class="sxs-lookup"><span data-stu-id="e370d-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="e370d-109">在特定目標應用程式或控制項上執行 AccChecker 驗證。</span><span class="sxs-lookup"><span data-stu-id="e370d-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="e370d-110">如需詳細資訊，請參閱 [ [驗證]](the-accchecker-graphical-user-interface.md)索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e370d-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="e370d-111">AccChecker 不會探索應用程式中的所有 UI 排列。</span><span class="sxs-lookup"><span data-stu-id="e370d-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="e370d-112">在視窗、窗格、索引標籤和功能表等控制項中隱藏的元素必須以手動方式公開。</span><span class="sxs-lookup"><span data-stu-id="e370d-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="e370d-113">檢查 AccChecker 錯誤記錄檔，並評估或分級結果。</span><span class="sxs-lookup"><span data-stu-id="e370d-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="e370d-114">修正簡單的問題，並適當地記錄嚴重的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e370d-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="e370d-115">針對可忽略的錯誤和錯誤產生隱藏專案檔，直到迴歸測試為止。</span><span class="sxs-lookup"><span data-stu-id="e370d-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="e370d-116">使用隱藏專案檔和初始錯誤修正來重新執行 AccChecker 驗證。</span><span class="sxs-lookup"><span data-stu-id="e370d-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="e370d-117">這會提供目前的 Microsoft Active Accessibility 執行問題的快照集，並建立迴歸測試的基準。</span><span class="sxs-lookup"><span data-stu-id="e370d-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="e370d-118">將 AccChecker Api 和隱藏專案整合到自動化測試架構中，以針對從初始 AccChecker 驗證記錄的 bug 進行迴歸測試。</span><span class="sxs-lookup"><span data-stu-id="e370d-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="e370d-119">修正錯誤時，應該視需要修改隱藏專案檔。</span><span class="sxs-lookup"><span data-stu-id="e370d-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="e370d-120">確認應用程式或控制項中未引進任何回歸或新的協助工具 bug。</span><span class="sxs-lookup"><span data-stu-id="e370d-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e370d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e370d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e370d-122">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="e370d-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




