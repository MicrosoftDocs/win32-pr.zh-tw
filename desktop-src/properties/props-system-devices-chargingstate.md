---
description: 裝置充電狀態。
ms.assetid: 33ef8ecb-29e3-4809-9d56-8d884f9c9ff6
title: ChargingState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de306cc44900849d74ba24924c9c4066c0ffe0a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027421"
---
# <a name="systemdeviceschargingstate"></a><span data-ttu-id="b8d47-103">ChargingState</span><span class="sxs-lookup"><span data-stu-id="b8d47-103">System.Devices.ChargingState</span></span>

<span data-ttu-id="b8d47-104">裝置充電狀態。</span><span class="sxs-lookup"><span data-stu-id="b8d47-104">Device charging status.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="b8d47-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="b8d47-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.ChargingState
   shellPKey = PKEY_Devices_ChargingState
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 11
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotCharging
            minValue = 0
            setValue = 0
            text = Not charging
            defineToken = CHARGINGSTATE_NOT_CHARGING
         enumRange
            name = Charging
            minValue = 1
            setValue = 1
            text = Charging
            defineToken = CHARGINGSTATE_CHARGING
         enumRange
            name = UnknownChargingState
            minValue = 2
            setValue = 2
            text = Unknown charging state
            defineToken = CHARGINGSTATE_UNKNOWN_STATE
```

## <a name="remarks"></a><span data-ttu-id="b8d47-106">備註</span><span class="sxs-lookup"><span data-stu-id="b8d47-106">Remarks</span></span>

<span data-ttu-id="b8d47-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="b8d47-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8d47-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8d47-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d47-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b8d47-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b8d47-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b8d47-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b8d47-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b8d47-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b8d47-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b8d47-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b8d47-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b8d47-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b8d47-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b8d47-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b8d47-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b8d47-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b8d47-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="b8d47-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b8d47-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b8d47-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b8d47-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b8d47-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b8d47-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="b8d47-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b8d47-120">editControl</span><span class="sxs-lookup"><span data-stu-id="b8d47-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b8d47-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="b8d47-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b8d47-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="b8d47-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
