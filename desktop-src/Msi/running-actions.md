---
description: 安裝程式函數可以用來執行特定動作或動作順序。
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: 執行動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981154"
---
# <a name="running-actions"></a><span data-ttu-id="a5104-103">執行動作</span><span class="sxs-lookup"><span data-stu-id="a5104-103">Running Actions</span></span>

<span data-ttu-id="a5104-104">安裝程式函數可以用來執行特定動作或動作順序。</span><span class="sxs-lookup"><span data-stu-id="a5104-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="a5104-105">這些動作可以是 [標準](standard-actions.md) 或 [自訂](custom-actions.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="a5104-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="a5104-106">下列程式說明如何執行動作：</span><span class="sxs-lookup"><span data-stu-id="a5104-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="a5104-107">**執行動作順序**</span><span class="sxs-lookup"><span data-stu-id="a5104-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="a5104-108">藉由呼叫 [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) 函數來執行資料表中定義的動作序列。</span><span class="sxs-lookup"><span data-stu-id="a5104-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="a5104-109">如果查詢的條件運算式評估為 TRUE，則安裝程式會查詢指定的資料表，並執行每個動作。</span><span class="sxs-lookup"><span data-stu-id="a5104-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="a5104-110">藉由呼叫 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數來檢查條件運算式。</span><span class="sxs-lookup"><span data-stu-id="a5104-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="a5104-111">藉由呼叫 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數來執行動作。</span><span class="sxs-lookup"><span data-stu-id="a5104-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="a5104-112">動作可以是標準動作、自訂動作或使用者介面對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a5104-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="a5104-113">如果在執行此動作期間發生錯誤，請呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="a5104-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="a5104-114">安裝程式將會處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5104-114">The installer will process the error.</span></span>

 

 



