---
title: 存取控制和讀取作業
description: 安全性是用於搜尋、列舉容器或讀取屬性的隱含篩選。
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- 存取控制和讀取作業 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020751"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="19776-104">存取控制和讀取作業</span><span class="sxs-lookup"><span data-stu-id="19776-104">Access Control and Read Operations</span></span>

<span data-ttu-id="19776-105">安全性是用於搜尋、列舉容器或讀取屬性的隱含篩選。</span><span class="sxs-lookup"><span data-stu-id="19776-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="19776-106">如果您沒有必要的存取權限，則嘗試列出物件或讀取屬性可能會失敗，並出現下列錯誤碼，即使物件或屬性存在也一樣：</span><span class="sxs-lookup"><span data-stu-id="19776-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="19776-107">**E \_ ADS \_ 不正確 \_ 網域 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="19776-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="19776-108">**\_ \_ \_ 不支援 E ADS \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="19776-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="19776-109">**\_ \_ \_ \_ 找不到電子 ADS 屬性**</span><span class="sxs-lookup"><span data-stu-id="19776-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="19776-110">請注意，具有 **\_ \_ ACTRL \_ DS \_ 清單** 存取權之 ADS 的呼叫者可以列舉容器中的子物件。</span><span class="sxs-lookup"><span data-stu-id="19776-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="19776-111">但是，如果呼叫者沒有 **ADS \_ 右邊 \_ ACTRL \_ DS \_ 清單 \_ 物件** 存取子物件，則嘗試存取子物件仍可能失敗並出現錯誤，例如 **E \_ ADS \_ 未知 \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="19776-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="19776-112">安全性對讀取作業的影響不一定會顯示為錯誤。</span><span class="sxs-lookup"><span data-stu-id="19776-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="19776-113">例如，搜尋作業可能會成功，但是搜尋結果不包含呼叫端沒有存取權的物件或屬性。</span><span class="sxs-lookup"><span data-stu-id="19776-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




