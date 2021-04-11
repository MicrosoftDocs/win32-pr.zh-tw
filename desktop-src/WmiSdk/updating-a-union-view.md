---
description: 您可以更新 union view 類別實例的非索引鍵屬性值。 您對 view 類別實例所做的變更將會傳播回組成 union view 類別的來源類別實例。
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: 更新聯集視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114844"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="020c2-104">更新聯集視圖</span><span class="sxs-lookup"><span data-stu-id="020c2-104">Updating a Union View</span></span>

<span data-ttu-id="020c2-105">您可以更新 union view 類別實例的非索引鍵屬性值。</span><span class="sxs-lookup"><span data-stu-id="020c2-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="020c2-106">您對 view 類別實例所做的變更將會傳播回組成 union view 類別的來源類別實例。</span><span class="sxs-lookup"><span data-stu-id="020c2-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="020c2-107">下列限制適用于 view 類別實例的變更：</span><span class="sxs-lookup"><span data-stu-id="020c2-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="020c2-108">您無法建立 view 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="020c2-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="020c2-109">只有 union 類別支援更新;聯結和相關檢視會建立唯讀的視圖實例。</span><span class="sxs-lookup"><span data-stu-id="020c2-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="020c2-110">更新成功與否取決於來源實例是否可更新。</span><span class="sxs-lookup"><span data-stu-id="020c2-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="020c2-111">如果視圖實例屬性對應至來源實例的唯讀屬性，則嘗試修改 view 屬性將會失敗。</span><span class="sxs-lookup"><span data-stu-id="020c2-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



