---
description: 表示所撰寫 DVD 內容的家長監護即將變更。
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: 'EC_DVD_PARENTAL_LEVEL_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992567"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="0d6e8-103">EC \_ DVD \_ 家長監護 \_ 層級 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="0d6e8-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="0d6e8-104">表示所撰寫 DVD 內容的家長監護即將變更。</span><span class="sxs-lookup"><span data-stu-id="0d6e8-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d6e8-105">參數</span><span class="sxs-lookup"><span data-stu-id="0d6e8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6e8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0d6e8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0d6e8-107">LONG 值，代表在播放玩家設定的新家長層級。</span><span class="sxs-lookup"><span data-stu-id="0d6e8-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="0d6e8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0d6e8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0d6e8-109">零個。</span><span class="sxs-lookup"><span data-stu-id="0d6e8-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d6e8-110">備註</span><span class="sxs-lookup"><span data-stu-id="0d6e8-110">Remarks</span></span>

<span data-ttu-id="0d6e8-111">[Dvd 流覽](dvd-navigator-filter.md)器篩選器在串流處理期間不支援家長監護變更，以回應 DVD 光碟上的 SetTmpPML 命令。</span><span class="sxs-lookup"><span data-stu-id="0d6e8-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6e8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d6e8-112">Requirements</span></span>



| <span data-ttu-id="0d6e8-113">需求</span><span class="sxs-lookup"><span data-stu-id="0d6e8-113">Requirement</span></span> | <span data-ttu-id="0d6e8-114">值</span><span class="sxs-lookup"><span data-stu-id="0d6e8-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6e8-115">標頭</span><span class="sxs-lookup"><span data-stu-id="0d6e8-115">Header</span></span><br/> | <dl> <span data-ttu-id="0d6e8-116"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="0d6e8-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d6e8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d6e8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6e8-118">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="0d6e8-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0d6e8-119">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="0d6e8-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0d6e8-120">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="0d6e8-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




