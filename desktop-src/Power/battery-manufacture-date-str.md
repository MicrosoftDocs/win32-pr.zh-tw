---
description: 包含電池製造日期。
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: 'BATTERY_MANUFACTURE_DATE 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980850"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="f2b43-103">電池 \_ 製造 \_ 日期結構</span><span class="sxs-lookup"><span data-stu-id="f2b43-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="f2b43-104">包含電池製造日期。</span><span class="sxs-lookup"><span data-stu-id="f2b43-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="f2b43-105">要求 BatteryManufactureDate 資訊層級時， [**電池 \_ 查詢 \_ 資訊**](battery-query-information-str.md) 結構會使用此結構。</span><span class="sxs-lookup"><span data-stu-id="f2b43-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b43-106">語法</span><span class="sxs-lookup"><span data-stu-id="f2b43-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="f2b43-107">成員</span><span class="sxs-lookup"><span data-stu-id="f2b43-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2b43-108">**Day**</span><span class="sxs-lookup"><span data-stu-id="f2b43-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="f2b43-109">製造月份的第一天，範圍介於1到31之間。</span><span class="sxs-lookup"><span data-stu-id="f2b43-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="f2b43-110">儘管是資料類型，但這不是 ASCII 編碼值。</span><span class="sxs-lookup"><span data-stu-id="f2b43-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="f2b43-111">它是不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="f2b43-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="f2b43-112">**月**</span><span class="sxs-lookup"><span data-stu-id="f2b43-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="f2b43-113">製造的月份，範圍 1 (1 月) 至 12 (12 月) 。</span><span class="sxs-lookup"><span data-stu-id="f2b43-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="f2b43-114">儘管是資料類型，但這不是 ASCII 編碼值。</span><span class="sxs-lookup"><span data-stu-id="f2b43-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="f2b43-115">它是不帶正負號的位元組。</span><span class="sxs-lookup"><span data-stu-id="f2b43-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="f2b43-116">**年**</span><span class="sxs-lookup"><span data-stu-id="f2b43-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="f2b43-117">製造的年份。</span><span class="sxs-lookup"><span data-stu-id="f2b43-117">The year of manufacture.</span></span> <span data-ttu-id="f2b43-118">這通常會在1900-2100 範圍內。</span><span class="sxs-lookup"><span data-stu-id="f2b43-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2b43-119">備註</span><span class="sxs-lookup"><span data-stu-id="f2b43-119">Remarks</span></span>

<span data-ttu-id="f2b43-120">日期是以西曆或西方日曆格式編碼。</span><span class="sxs-lookup"><span data-stu-id="f2b43-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b43-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2b43-121">Requirements</span></span>



| <span data-ttu-id="f2b43-122">需求</span><span class="sxs-lookup"><span data-stu-id="f2b43-122">Requirement</span></span> | <span data-ttu-id="f2b43-123">值</span><span class="sxs-lookup"><span data-stu-id="f2b43-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b43-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2b43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b43-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2b43-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="f2b43-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2b43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b43-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2b43-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="f2b43-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f2b43-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b43-129"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b43-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b43-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2b43-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b43-131">**電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f2b43-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="f2b43-132">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f2b43-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




