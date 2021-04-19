---
description: LINEPARKMODE \_ 位旗標常數描述停車呼叫的不同方式。
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: 'LINEPARKMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978450"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="29637-103">LINEPARKMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="29637-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="29637-104">**LINEPARKMODE \_** 位旗標常數描述停車呼叫的不同方式。</span><span class="sxs-lookup"><span data-stu-id="29637-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="29637-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="29637-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="29637-106">指定導向撥打電話。</span><span class="sxs-lookup"><span data-stu-id="29637-106">Specifies directed call park.</span></span> <span data-ttu-id="29637-107">要暫停呼叫的位址必須提供給參數。</span><span class="sxs-lookup"><span data-stu-id="29637-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="29637-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ NONDIRECTED**</span><span class="sxs-lookup"><span data-stu-id="29637-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="29637-109">指定 nondirected 呼叫公園。</span><span class="sxs-lookup"><span data-stu-id="29637-109">Specifies nondirected call park.</span></span> <span data-ttu-id="29637-110">切換時，會選取要放置呼叫的位址，並由參數提供給應用程式。</span><span class="sxs-lookup"><span data-stu-id="29637-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29637-111">備註</span><span class="sxs-lookup"><span data-stu-id="29637-111">Remarks</span></span>

<span data-ttu-id="29637-112">無延伸。</span><span class="sxs-lookup"><span data-stu-id="29637-112">No extensibility.</span></span> <span data-ttu-id="29637-113">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="29637-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="29637-114">在停車呼叫時，會使用 **LINEPARKMODE \_ 常數** 。</span><span class="sxs-lookup"><span data-stu-id="29637-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="29637-115">請參閱線路的位址裝置功能，找出可用的公園模式。</span><span class="sxs-lookup"><span data-stu-id="29637-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="29637-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="29637-116">Requirements</span></span>



| <span data-ttu-id="29637-117">需求</span><span class="sxs-lookup"><span data-stu-id="29637-117">Requirement</span></span> | <span data-ttu-id="29637-118">值</span><span class="sxs-lookup"><span data-stu-id="29637-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29637-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="29637-119">TAPI version</span></span><br/> | <span data-ttu-id="29637-120">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="29637-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="29637-121">標頭</span><span class="sxs-lookup"><span data-stu-id="29637-121">Header</span></span><br/>       | <dl> <span data-ttu-id="29637-122"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="29637-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




