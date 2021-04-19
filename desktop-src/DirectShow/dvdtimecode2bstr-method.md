---
description: DVDTimeCode2bstr 方法會抓取表示光碟上目前時間的字串。
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: DVDTimeCode2bstr 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986228"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="2b945-103">DVDTimeCode2bstr 方法</span><span class="sxs-lookup"><span data-stu-id="2b945-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="2b945-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="2b945-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2b945-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="2b945-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2b945-106">方法會抓取 `DVDTimeCode2bstr` 表示光碟上目前時間的字串。</span><span class="sxs-lookup"><span data-stu-id="2b945-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="2b945-107">參數</span><span class="sxs-lookup"><span data-stu-id="2b945-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b945-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span><span class="sxs-lookup"><span data-stu-id="2b945-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="2b945-109">指定光碟上的目前時間，其相對於標題開頭為透過 [**EC \_ DVD \_ 目前 \_ HMSF \_ 時間**](ec-dvd-current-hmsf-time.md) 事件取得的數位。</span><span class="sxs-lookup"><span data-stu-id="2b945-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b945-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b945-110">Return Value</span></span>

<span data-ttu-id="2b945-111">傳回11個字元的字串，格式為 "hh： mm： ss： ff"，代表定義目前時間的時、分、秒和框架。</span><span class="sxs-lookup"><span data-stu-id="2b945-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b945-112">備註</span><span class="sxs-lookup"><span data-stu-id="2b945-112">Remarks</span></span>

<span data-ttu-id="2b945-113">這個方法是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2b945-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b945-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b945-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b945-115">處理 DVD 事件通知</span><span class="sxs-lookup"><span data-stu-id="2b945-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



