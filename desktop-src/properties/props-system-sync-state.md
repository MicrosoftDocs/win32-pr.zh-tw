---
description: 系統同步處理的狀態。
ms.assetid: e7659752-ba8c-4b3b-bd1e-2f5044a3ab47
title: System. Sync. State
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4b245490aec4aa7df0975e921f6a8b9ba0af28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513556"
---
# <a name="systemsyncstate"></a><span data-ttu-id="132ff-103">System. Sync. State</span><span class="sxs-lookup"><span data-stu-id="132ff-103">System.Sync.State</span></span>

<span data-ttu-id="132ff-104">系統同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="132ff-104">State of the system synch.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="132ff-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="132ff-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Sync.State
   shellPKey = PKEY_Sync_State
   formatID = 7BD5533E-AF15-44DB-B8C8-BD6624E1D032
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotSetup
            value = 0
            text = Setup sync
            defineToken = SYNC_STATE_NOTSETUP
         enum
            name = NotRun
            value = 1
            text = Not synced yet
            defineToken = SYNC_STATE_SYNCNOTRUN
         enum
            name = Idle
            value = 2
            text = Not synced yet
            defineToken = SYNC_STATE_IDLE
         enum
            name = SyncErrors
            value = 3
            text = Synced with errors
            defineToken = SYNC_STATE_ERROR
         enum
            name = Pending
            value = 4
            text = Sync pending
            defineToken = SYNC_STATE_PENDING
         enum
            name = Syncing
            value = 5
            text = Syncing
            defineToken = SYNC_STATE_SYNCING
```

## <a name="remarks"></a><span data-ttu-id="132ff-106">備註</span><span class="sxs-lookup"><span data-stu-id="132ff-106">Remarks</span></span>

<span data-ttu-id="132ff-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="132ff-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="132ff-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="132ff-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="132ff-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="132ff-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="132ff-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="132ff-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="132ff-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="132ff-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="132ff-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="132ff-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="132ff-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="132ff-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="132ff-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="132ff-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="132ff-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="132ff-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="132ff-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="132ff-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="132ff-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="132ff-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="132ff-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="132ff-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="132ff-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="132ff-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="132ff-120">editControl</span><span class="sxs-lookup"><span data-stu-id="132ff-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="132ff-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="132ff-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="132ff-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="132ff-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
