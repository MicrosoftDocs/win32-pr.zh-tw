---
description: LaunchConditions 動作會查詢 LaunchCondition 資料表，並評估記錄在該處的每個條件陳述式。 如果上述任一條件陳述式失敗，則會向使用者顯示錯誤訊息，並結束安裝。
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: LaunchConditions 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966719"
---
# <a name="launchconditions-action"></a><span data-ttu-id="3130c-104">LaunchConditions 動作</span><span class="sxs-lookup"><span data-stu-id="3130c-104">LaunchConditions Action</span></span>

<span data-ttu-id="3130c-105">LaunchConditions 動作會查詢 [LaunchCondition 資料表](launchcondition-table.md) ，並評估記錄在該處的每個條件陳述式。</span><span class="sxs-lookup"><span data-stu-id="3130c-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="3130c-106">如果上述任一條件陳述式失敗，則會向使用者顯示錯誤訊息，並結束安裝。</span><span class="sxs-lookup"><span data-stu-id="3130c-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3130c-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="3130c-107">Sequence Restrictions</span></span>

<span data-ttu-id="3130c-108">LaunchConditions 動作是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3130c-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="3130c-109">此動作通常是序列中的第一個動作，但 [AppSearch 動作](appsearch-action.md) 可能會在 LaunchConditions 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="3130c-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="3130c-110">如果沒有適用于所有安裝模式的啟動條件，則應該在適當的順序資料表中的條件運算式中使用適當的安裝模式屬性。</span><span class="sxs-lookup"><span data-stu-id="3130c-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3130c-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="3130c-111">ActionData Messages</span></span>

<span data-ttu-id="3130c-112">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="3130c-112">There are no ActionData messages.</span></span>

 

 



