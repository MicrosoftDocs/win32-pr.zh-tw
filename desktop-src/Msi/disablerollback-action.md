---
description: DisableRollback 動作會停用其餘安裝的復原。
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: DisableRollback 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740e838a6dca2d97db616703faf24c590ab69bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113865"
---
# <a name="disablerollback-action"></a><span data-ttu-id="edca0-103">DisableRollback 動作</span><span class="sxs-lookup"><span data-stu-id="edca0-103">DisableRollback Action</span></span>

<span data-ttu-id="edca0-104">DisableRollback 動作會停用其餘安裝的 [復原](rollback-installation.md) 。</span><span class="sxs-lookup"><span data-stu-id="edca0-104">The DisableRollback Action disables [rollback](rollback-installation.md) for the remainder of the installation.</span></span> <span data-ttu-id="edca0-105">只有在順序資料表中的 DisableRollback 動作之後排序的動作才會停用復原。</span><span class="sxs-lookup"><span data-stu-id="edca0-105">Rollback is disabled only for the actions that are sequenced after the DisableRollback action in the sequence tables.</span></span> <span data-ttu-id="edca0-106">如果 DisableRollback 動作是在 [InstallInitialize 動作](installinitialize-action.md)之前排序，則會停用整個安裝的復原。</span><span class="sxs-lookup"><span data-stu-id="edca0-106">Rollback is disabled for the entire installation if the DisableRollback action is sequenced before the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="edca0-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="edca0-107">Sequence Restrictions</span></span>

<span data-ttu-id="edca0-108">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="edca0-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-message"></a><span data-ttu-id="edca0-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="edca0-109">ActionData Message</span></span>

<span data-ttu-id="edca0-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="edca0-110">There are no ActionData messages.</span></span>

 

 



