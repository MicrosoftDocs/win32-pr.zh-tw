---
description: 要變更系統狀態的自訂動作必須是延後執行自訂動作。
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: 使用自訂動作變更系統狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993095"
---
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="689e6-103">使用自訂動作變更系統狀態</span><span class="sxs-lookup"><span data-stu-id="689e6-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="689e6-104">要變更系統狀態的自訂動作必須是延後執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="689e6-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="689e6-105">藉由將資料列插入至順序資料表來設定屬性、功能狀態、元件狀態或目標目錄或排程系統作業的自訂動作，可以安全地使用立即執行。</span><span class="sxs-lookup"><span data-stu-id="689e6-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="689e6-106">不過，直接變更系統或呼叫另一個系統服務的自訂動作，必須延後至執行安裝腳本的時間。</span><span class="sxs-lookup"><span data-stu-id="689e6-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="689e6-107">如需詳細資訊，請參閱 [延後執行自訂動作](deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="689e6-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="689e6-108">您不應該嘗試使用立即執行自訂動作來變更系統狀態，因為每個變更狀態的自訂動作都必須有對應的復原自訂動作，才能在安裝復原時復原系統狀態變更。</span><span class="sxs-lookup"><span data-stu-id="689e6-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="689e6-109">所有的復原自訂動作也都是延後的自訂動作，而且必須在其復原的動作之前。</span><span class="sxs-lookup"><span data-stu-id="689e6-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="689e6-110">如需詳細資訊，請參閱 [復原自訂動作](rollback-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="689e6-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



