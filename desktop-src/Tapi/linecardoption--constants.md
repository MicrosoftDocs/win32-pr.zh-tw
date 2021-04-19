---
description: LINECARDOPTION \_ 常數會定義 LINECARDENTRY 結構的 >dwoptions 成員所使用的值，這些值會在 lineGetTranslateCaps 所傳回之 LINETRANSLATECAPS 結構的一部分傳回。
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: 'LINECARDOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994909"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="1a0a3-103">LINECARDOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="1a0a3-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="1a0a3-104">**LINECARDOPTION \_ 常數** 會定義 [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry)結構的 **>dwoptions** 成員所使用的值，這些值會在 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)所傳回之 [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)結構的一部分傳回。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="1a0a3-105">**LINECARDOPTION \_ 常數** t 具有下列值：</span><span class="sxs-lookup"><span data-stu-id="1a0a3-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1a0a3-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**\_隱藏 LINECARDOPTION**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a0a3-107">使用者已隱藏此電話卡。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="1a0a3-108">撥號協助程式未顯示在可用電話卡的主要清單中，但會顯示在可從中複製撥號規則的卡片清單中。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a0a3-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ 預先定義**</span><span class="sxs-lookup"><span data-stu-id="1a0a3-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a0a3-110">這張電話卡是 Microsoft 電話語音隨附的其中一個預先定義的電話卡定義。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="1a0a3-111">無法使用撥號協助程式完全移除：如果使用者嘗試移除它，就會變成隱藏狀態。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="1a0a3-112">如此一來，就可以繼續存取撥號規則。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a0a3-113">備註</span><span class="sxs-lookup"><span data-stu-id="1a0a3-113">Remarks</span></span>

<span data-ttu-id="1a0a3-114">不可延伸。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-114">Not extensible.</span></span> <span data-ttu-id="1a0a3-115">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="1a0a3-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0a3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a0a3-116">Requirements</span></span>



| <span data-ttu-id="1a0a3-117">需求</span><span class="sxs-lookup"><span data-stu-id="1a0a3-117">Requirement</span></span> | <span data-ttu-id="1a0a3-118">值</span><span class="sxs-lookup"><span data-stu-id="1a0a3-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1a0a3-119">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1a0a3-119">TAPI version</span></span><br/> | <span data-ttu-id="1a0a3-120">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1a0a3-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1a0a3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1a0a3-121">Header</span></span><br/>       | <dl> <span data-ttu-id="1a0a3-122"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="1a0a3-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




