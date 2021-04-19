---
description: LINETRANSFERMODE \_ 位旗標常數描述解決呼叫傳輸要求的不同方式。
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: 'LINETRANSFERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989709"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="2e2a4-103">LINETRANSFERMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="2e2a4-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="2e2a4-104">**LINETRANSFERMODE \_** 位旗標常數描述解決呼叫傳輸要求的不同方式。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="2e2a4-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE \_ 會議**</span><span class="sxs-lookup"><span data-stu-id="2e2a4-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e2a4-106">藉由在應用程式、連線至初始通話的合作物件，以及連線到諮詢通話的合作物件之間建立三向會議，即可解決此轉移。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="2e2a4-107">選取此選項時，就會建立會議通話。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e2a4-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="2e2a4-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e2a4-109">傳輸的解決方式是將初始呼叫傳送給諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="2e2a4-110">這兩個呼叫都會變成閒置的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e2a4-111">備註</span><span class="sxs-lookup"><span data-stu-id="2e2a4-111">Remarks</span></span>

<span data-ttu-id="2e2a4-112">無延伸。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-112">No extensibility.</span></span> <span data-ttu-id="2e2a4-113">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="2e2a4-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2a4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e2a4-114">Requirements</span></span>



| <span data-ttu-id="2e2a4-115">需求</span><span class="sxs-lookup"><span data-stu-id="2e2a4-115">Requirement</span></span> | <span data-ttu-id="2e2a4-116">值</span><span class="sxs-lookup"><span data-stu-id="2e2a4-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2e2a4-117">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2e2a4-117">TAPI version</span></span><br/> | <span data-ttu-id="2e2a4-118">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2e2a4-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2e2a4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2e2a4-119">Header</span></span><br/>       | <dl> <span data-ttu-id="2e2a4-120"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="2e2a4-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




