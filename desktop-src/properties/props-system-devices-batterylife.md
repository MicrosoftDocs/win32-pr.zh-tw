---
description: 剩餘的電池壽命（以百分比表示）。
ms.assetid: b6f4f5d6-7f12-4104-95ad-b163445d198b
title: System.Devices.BatteryLife
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8f24f5ecaa78231fdc463b718046adc42fc681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001408"
---
# <a name="systemdevicesbatterylife"></a><span data-ttu-id="c6ba6-103">System.Devices.BatteryLife</span><span class="sxs-lookup"><span data-stu-id="c6ba6-103">System.Devices.BatteryLife</span></span>

<span data-ttu-id="c6ba6-104">剩餘的電池壽命（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="c6ba6-104">Remaining battery life, as a percentage.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="c6ba6-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="c6ba6-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.BatteryLife
   shellPKey = PKEY_Devices_BatteryLife
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = CriticallyLow
            minValue = 0
            setValue = 5
            text = Critically low battery
            defineToken = BATTERYLIFE_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 11
            setValue = 18
            text = Low battery
            defineToken = BATTERYLIFE_LOW
         enumRange
            name = Average
            minValue = 26
            setValue = 60
            text = Average battery
            defineToken = BATTERYLIFE_AVERAGE
         enumRange
            name = Full
            minValue = 90
            setValue = 95
            text = Full battery
            defineToken = BATTERYLIFE_FULL
         enumRange
            name = UnknownStatus
            minValue = 101
            setValue = 101
            text = Unknown battery status
            defineToken = BATTERYLIFE_UNKNOWN_STATUS
```

## <a name="remarks"></a><span data-ttu-id="c6ba6-106">備註</span><span class="sxs-lookup"><span data-stu-id="c6ba6-106">Remarks</span></span>

<span data-ttu-id="c6ba6-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="c6ba6-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6ba6-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6ba6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6ba6-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c6ba6-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c6ba6-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c6ba6-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c6ba6-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c6ba6-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c6ba6-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c6ba6-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="c6ba6-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c6ba6-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c6ba6-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="c6ba6-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-120">editControl</span><span class="sxs-lookup"><span data-stu-id="c6ba6-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="c6ba6-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c6ba6-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="c6ba6-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
