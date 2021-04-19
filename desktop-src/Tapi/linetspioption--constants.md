---
description: LINETSPIOPTION \_ 常數描述應呼叫的訂單服務提供者。
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: 'LINETSPIOPTION_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999538"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="36917-103">LINETSPIOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="36917-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="36917-104">**LINETSPIOPTION \_ 常數** 描述應呼叫的訂單服務提供者。</span><span class="sxs-lookup"><span data-stu-id="36917-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="36917-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**</span><span class="sxs-lookup"><span data-stu-id="36917-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36917-106">TAPI 應一次呼叫此服務提供者中的函式;它應該等候每個函式傳回 (但不是非同步函式，以便在相同或不同的處理器上，于相同或不同的執行緒上呼叫相同或不同的函式，以完成) 。</span><span class="sxs-lookup"><span data-stu-id="36917-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36917-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="36917-107">Requirements</span></span>



| <span data-ttu-id="36917-108">需求</span><span class="sxs-lookup"><span data-stu-id="36917-108">Requirement</span></span> | <span data-ttu-id="36917-109">值</span><span class="sxs-lookup"><span data-stu-id="36917-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="36917-110">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="36917-110">TAPI version</span></span><br/> | <span data-ttu-id="36917-111">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="36917-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="36917-112">標頭</span><span class="sxs-lookup"><span data-stu-id="36917-112">Header</span></span><br/>       | <dl> <span data-ttu-id="36917-113"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="36917-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




