---
description: DVDNotify 事件會通知應用程式有許多不同的 DVD 事件和光碟指令。
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: 'DVDNotify (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989856"
---
# <a name="dvdnotify"></a><span data-ttu-id="681fa-103">DVDNotify</span><span class="sxs-lookup"><span data-stu-id="681fa-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="681fa-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="681fa-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="681fa-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="681fa-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="681fa-106">此 `DVDNotify` 事件會通知應用程式有許多不同的 DVD 事件和光碟指令。</span><span class="sxs-lookup"><span data-stu-id="681fa-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="681fa-107">參數</span><span class="sxs-lookup"><span data-stu-id="681fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681fa-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="681fa-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="681fa-109">指定 DVD 事件通知碼。</span><span class="sxs-lookup"><span data-stu-id="681fa-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="681fa-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span><span class="sxs-lookup"><span data-stu-id="681fa-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="681fa-111">可以包含與事件相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="681fa-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="681fa-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="681fa-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="681fa-113">可以包含與事件相關的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="681fa-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="681fa-114">備註</span><span class="sxs-lookup"><span data-stu-id="681fa-114">Remarks</span></span>

<span data-ttu-id="681fa-115">[Dvd 事件通知代碼](dvd-notification-codes.md) 提供所有 DVD 事件通知碼及其參數的完整說明。</span><span class="sxs-lookup"><span data-stu-id="681fa-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="681fa-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="681fa-116">Requirements</span></span>



| <span data-ttu-id="681fa-117">需求</span><span class="sxs-lookup"><span data-stu-id="681fa-117">Requirement</span></span> | <span data-ttu-id="681fa-118">值</span><span class="sxs-lookup"><span data-stu-id="681fa-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="681fa-119">標頭</span><span class="sxs-lookup"><span data-stu-id="681fa-119">Header</span></span><br/> | <dl> <span data-ttu-id="681fa-120"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="681fa-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




