---
description: 裝置上的可用儲存空間總計（以百分比表示）。
ms.assetid: ede845c6-abd8-4bb1-b0d8-c1f3facffa41
title: StorageFreeSpacePercent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df717e488d1fabac811a2629a75160a2e7f81df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944092"
---
# <a name="systemdevicesstoragefreespacepercent"></a><span data-ttu-id="4075e-103">StorageFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="4075e-103">System.Devices.StorageFreeSpacePercent</span></span>

<span data-ttu-id="4075e-104">裝置上的可用儲存空間總計（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="4075e-104">Total free storage space on the device, as a percentage.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4075e-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="4075e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.StorageFreeSpacePercent
   shellPKey = PKEY_Devices_StorageFreeSpacePercent
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 14
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = StorageSpaceFull
            minValue = 0
            setValue = 0
            text = Storage space full
            defineToken = STORAGESPACE_FULL
         enumRange
            name = 5PercentFree
            minValue = 5
            setValue = 5
            text = 5% free space
            defineToken = STORAGESPACE_5_PERCENT
         enumRange
            name = 10PercentFree
            minValue = 10
            setValue = 10
            text = 10% free space
            defineToken = STORAGESPACE_10_PERCENT
```

## <a name="remarks"></a><span data-ttu-id="4075e-106">備註</span><span class="sxs-lookup"><span data-stu-id="4075e-106">Remarks</span></span>

<span data-ttu-id="4075e-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="4075e-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4075e-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="4075e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4075e-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4075e-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4075e-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4075e-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4075e-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4075e-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4075e-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4075e-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4075e-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4075e-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4075e-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4075e-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4075e-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4075e-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4075e-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="4075e-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4075e-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4075e-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4075e-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4075e-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4075e-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="4075e-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4075e-120">editControl</span><span class="sxs-lookup"><span data-stu-id="4075e-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4075e-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="4075e-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4075e-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="4075e-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
