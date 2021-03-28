---
description: 這是即時會話中遺失之事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 09ffcc4d-916f-458d-91c6-a261776092d2
title: Lost_Event 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Lost_Event
api_type:
- NA
api_location: ''
ms.openlocfilehash: cbf52e76d9cd84ea53ec0ecd124279d159a2cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512192"
---
# <a name="lost_event-class"></a><span data-ttu-id="d92ad-104">遺失 \_ 事件類別</span><span class="sxs-lookup"><span data-stu-id="d92ad-104">Lost\_Event class</span></span>

<span data-ttu-id="d92ad-105">這是即時會話中遺失之事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="d92ad-105">This is the parent class for events lost in a real-time session.</span></span>

<span data-ttu-id="d92ad-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d92ad-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="d92ad-107">Syntax</span></span>

``` syntax
[Guid("{6a399ae0-4bc6-4de9-870b-3657f8947e7e}")]
class Lost_Event : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d92ad-108">成員</span><span class="sxs-lookup"><span data-stu-id="d92ad-108">Members</span></span>

<span data-ttu-id="d92ad-109">**遺失的 \_ 事件** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="d92ad-109">The **Lost\_Event** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92ad-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d92ad-110">Requirements</span></span>



| <span data-ttu-id="d92ad-111">需求</span><span class="sxs-lookup"><span data-stu-id="d92ad-111">Requirement</span></span> | <span data-ttu-id="d92ad-112">值</span><span class="sxs-lookup"><span data-stu-id="d92ad-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d92ad-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d92ad-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d92ad-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d92ad-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d92ad-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d92ad-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d92ad-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d92ad-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d92ad-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d92ad-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92ad-118">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="d92ad-118">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="d92ad-119">**RT \_ LostEvent**</span><span class="sxs-lookup"><span data-stu-id="d92ad-119">**RT\_LostEvent**</span></span>](rt-lostevent.md)
</dt> </dl>

 

 




