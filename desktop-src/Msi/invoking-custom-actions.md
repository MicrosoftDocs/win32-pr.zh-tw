---
description: 自訂動作的叫用方式與標準動作相同，無論是明確調用或在順序資料表執行期間。
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: 叫用自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988428"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="2ff4e-103">叫用自訂動作</span><span class="sxs-lookup"><span data-stu-id="2ff4e-103">Invoking Custom Actions</span></span>

<span data-ttu-id="2ff4e-104">自訂動作的叫用方式與標準動作相同，無論是明確調用或在順序資料表執行期間。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="2ff4e-105">呼叫動作的方法有兩種：</span><span class="sxs-lookup"><span data-stu-id="2ff4e-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="2ff4e-106">您可以使用 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數直接呼叫指定的動作。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="2ff4e-107">最上層動作會呼叫包含自訂動作的順序資料表。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="2ff4e-108">如需有關排程順序資料表中自訂動作的詳細資訊，請參閱 [排序自訂動作](sequencing-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="2ff4e-109">當安裝程式從 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函式或順序資料表取得動作名稱時，它會先搜尋該名稱的標準動作。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="2ff4e-110">如果找不到標準動作，則安裝程式會查詢 [CustomAction 資料表](customaction-table.md) ，以檢查指定的動作是否為自訂動作。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="2ff4e-111">如果指定的動作不是自訂動作，則安裝程式會查詢對話方塊 [資料表](dialog-table.md) 中的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2ff4e-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



