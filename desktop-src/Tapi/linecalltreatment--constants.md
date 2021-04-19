---
description: LINECALLTREATMENT \_ 常數會列出未接聽或保留的呼叫的進行中的操作。 除了基本參數驗證，呼叫處理是由 TAPI 直接傳遞給服務提供者。
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: 'LINECALLTREATMENT_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995483"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="a710c-104">LINECALLTREATMENT \_ 常數</span><span class="sxs-lookup"><span data-stu-id="a710c-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="a710c-105">**LINECALLTREATMENT \_** 常數會列出未接聽或保留的呼叫的進行中的操作。</span><span class="sxs-lookup"><span data-stu-id="a710c-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="a710c-106">除了基本參數驗證，呼叫處理是由 TAPI 直接傳遞給服務提供者。</span><span class="sxs-lookup"><span data-stu-id="a710c-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="a710c-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="a710c-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a710c-108">當呼叫未主動連線到裝置 (供應或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到忙碌信號。</span><span class="sxs-lookup"><span data-stu-id="a710c-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a710c-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT \_ 音樂**</span><span class="sxs-lookup"><span data-stu-id="a710c-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a710c-110">當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到音樂。</span><span class="sxs-lookup"><span data-stu-id="a710c-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a710c-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ 回電**</span><span class="sxs-lookup"><span data-stu-id="a710c-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a710c-112">當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到回電語氣。</span><span class="sxs-lookup"><span data-stu-id="a710c-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a710c-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ 無聲**</span><span class="sxs-lookup"><span data-stu-id="a710c-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a710c-114">當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到無聲。</span><span class="sxs-lookup"><span data-stu-id="a710c-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a710c-115">備註</span><span class="sxs-lookup"><span data-stu-id="a710c-115">Remarks</span></span>

<span data-ttu-id="a710c-116">保留值0x00000000 以表示服務提供者不支援呼叫處理。</span><span class="sxs-lookup"><span data-stu-id="a710c-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="a710c-117">範圍0x00000005 到0x000000FF 的值會保留供未來定義之用。</span><span class="sxs-lookup"><span data-stu-id="a710c-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="a710c-118">範圍0x00000100 到0xFFFFFFFF 的值會保留給服務提供者指派，而且可能包含特定的音樂選擇或記錄的宣告。</span><span class="sxs-lookup"><span data-stu-id="a710c-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="a710c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a710c-119">Requirements</span></span>



| <span data-ttu-id="a710c-120">需求</span><span class="sxs-lookup"><span data-stu-id="a710c-120">Requirement</span></span> | <span data-ttu-id="a710c-121">值</span><span class="sxs-lookup"><span data-stu-id="a710c-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a710c-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a710c-122">TAPI version</span></span><br/> | <span data-ttu-id="a710c-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a710c-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a710c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a710c-124">Header</span></span><br/>       | <dl> <span data-ttu-id="a710c-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="a710c-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




