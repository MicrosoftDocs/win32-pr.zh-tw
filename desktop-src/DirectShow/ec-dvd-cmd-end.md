---
description: 表示特定 DVD 導覽器命令已完成。
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: 'EC_DVD_CMD_END (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998710"
---
# <a name="ec_dvd_cmd_end"></a><span data-ttu-id="4d930-103">EC \_ DVD \_ CMD \_ END</span><span class="sxs-lookup"><span data-stu-id="4d930-103">EC\_DVD\_CMD\_END</span></span>

<span data-ttu-id="4d930-104">表示特定 DVD 導覽 [器](dvd-navigator-filter.md) 命令已完成。</span><span class="sxs-lookup"><span data-stu-id="4d930-104">Signals that a particular [DVD Navigator](dvd-navigator-filter.md) command has completed.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d930-105">參數</span><span class="sxs-lookup"><span data-stu-id="4d930-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d930-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4d930-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4d930-107">命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d930-107">Command identifier.</span></span> <span data-ttu-id="4d930-108">將此參數傳遞給 [**IDvdInfo2：： GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) 方法，以取得 [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4d930-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="4d930-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4d930-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4d930-110">**HRESULT** 值，指出命令的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d930-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d930-111">備註</span><span class="sxs-lookup"><span data-stu-id="4d930-111">Remarks</span></span>

<span data-ttu-id="4d930-112">只有當您的應用程式 \_ \_ \_ 在採用 [**dvd \_ cmd \_ 旗標旗標**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)的 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)方法中設定 DVD cmd 旗標 SendEvents 旗標時，才會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="4d930-112">This event is only fired if your application sets the DVD\_CMD\_FLAG\_SendEvents flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="4d930-113">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="4d930-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d930-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d930-114">Requirements</span></span>



| <span data-ttu-id="4d930-115">需求</span><span class="sxs-lookup"><span data-stu-id="4d930-115">Requirement</span></span> | <span data-ttu-id="4d930-116">值</span><span class="sxs-lookup"><span data-stu-id="4d930-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d930-117">標頭</span><span class="sxs-lookup"><span data-stu-id="4d930-117">Header</span></span><br/> | <dl> <span data-ttu-id="4d930-118"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="4d930-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d930-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d930-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d930-120">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="4d930-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="4d930-121">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="4d930-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4d930-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="4d930-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="4d930-123">同步處理 DVD 命令</span><span class="sxs-lookup"><span data-stu-id="4d930-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




