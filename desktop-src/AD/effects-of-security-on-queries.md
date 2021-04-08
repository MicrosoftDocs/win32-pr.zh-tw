---
title: 搜尋安全性的影響
description: 安全性是執行搜尋、列舉容器或讀取屬性時的隱含篩選。
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- 搜尋 Active Directory 的安全性效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671332"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="903f5-104">搜尋安全性的影響</span><span class="sxs-lookup"><span data-stu-id="903f5-104">Effects of Security on Searching</span></span>

<span data-ttu-id="903f5-105">安全性是執行搜尋、列舉容器或讀取屬性時的隱含篩選。</span><span class="sxs-lookup"><span data-stu-id="903f5-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="903f5-106">即使您沒有讀取物件之屬性的存取權，ADSI 也可以傳回沒有 \_ 這類 \_ 屬性或沒有 \_ 這類 \_ 物件錯誤。</span><span class="sxs-lookup"><span data-stu-id="903f5-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="903f5-107">例如，呼叫端可能會列舉容器中的子物件，因為呼叫端在容器上具有清單 \_ 內容許可權。</span><span class="sxs-lookup"><span data-stu-id="903f5-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="903f5-108">但是，如果呼叫端沒有子物件的讀取權限，則相同的呼叫端可能無法存取列舉物件。</span><span class="sxs-lookup"><span data-stu-id="903f5-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="903f5-109">在此情況下， \_ \_ 即使呼叫端已成功列舉物件，子物件的查詢也可能不會傳回此物件。</span><span class="sxs-lookup"><span data-stu-id="903f5-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="903f5-110">如果呼叫端沒有足夠的許可權，可能會傳回下列傳回碼：</span><span class="sxs-lookup"><span data-stu-id="903f5-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="903f5-111">E \_ ADS \_ 不正確 \_ 網域 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="903f5-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="903f5-112">\_ \_ \_ 不支援 E ADS \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="903f5-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="903f5-113">\_ \_ \_ \_ 找不到電子 ADS 屬性</span><span class="sxs-lookup"><span data-stu-id="903f5-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




