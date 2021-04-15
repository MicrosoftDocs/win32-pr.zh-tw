---
title: 處理保留
description: URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383210"
---
# <a name="processing-reservations"></a><span data-ttu-id="eec68-103">處理保留</span><span class="sxs-lookup"><span data-stu-id="eec68-103">Processing Reservations</span></span>

<span data-ttu-id="eec68-104">URL 命名空間部分的保留專案是由系統管理員所建立，並放在持續性保留存放區中。</span><span class="sxs-lookup"><span data-stu-id="eec68-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="eec68-105">HTTP 的 URL 命名空間的根目錄是由系統管理員所擁有。</span><span class="sxs-lookup"><span data-stu-id="eec68-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="eec68-106">針對所有主機和埠值，一律會在 **relativeUri** 命名空間的根目錄採用下列兩個保留。</span><span class="sxs-lookup"><span data-stu-id="eec68-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="eec68-107">命名空間保留</span><span class="sxs-lookup"><span data-stu-id="eec68-107">Namespace reserved</span></span>                 | <span data-ttu-id="eec68-108">保留給</span><span class="sxs-lookup"><span data-stu-id="eec68-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="eec68-109"> HTTPs:// <host> ：<port>/</span><span class="sxs-lookup"><span data-stu-id="eec68-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="eec68-110">LocalSystem 系統管理員</span><span class="sxs-lookup"><span data-stu-id="eec68-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="eec68-111"> HTTPs:// <host> ：<port>/</span><span class="sxs-lookup"><span data-stu-id="eec68-111">https://<host>:<port>/</span></span> | <span data-ttu-id="eec68-112">LocalSystem 系統管理員</span><span class="sxs-lookup"><span data-stu-id="eec68-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="eec68-113">無法移除這些隱含的保留。</span><span class="sxs-lookup"><span data-stu-id="eec68-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="eec68-114">不過，您可以將明確的根保留委派給其他使用者。</span><span class="sxs-lookup"><span data-stu-id="eec68-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="eec68-115">如下所示的保留會建立這類委派：</span><span class="sxs-lookup"><span data-stu-id="eec68-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="eec68-116">命名空間保留</span><span class="sxs-lookup"><span data-stu-id="eec68-116">Namespace reserved</span></span>        | <span data-ttu-id="eec68-117">保留給</span><span class="sxs-lookup"><span data-stu-id="eec68-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="eec68-118">UserA、UserC</span><span class="sxs-lookup"><span data-stu-id="eec68-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="eec68-119">UserB</span><span class="sxs-lookup"><span data-stu-id="eec68-119">UserB</span></span>        |



 

<span data-ttu-id="eec68-120">如果系統管理員移除這些委派的保留專案，命名空間的擁有權會還原為對應主機和埠值的隱含保留。</span><span class="sxs-lookup"><span data-stu-id="eec68-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




