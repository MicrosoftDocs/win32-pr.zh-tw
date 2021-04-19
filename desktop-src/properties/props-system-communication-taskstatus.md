---
description: 表示工作的目前狀態。
ms.assetid: 76bb9bb7-3383-4e5a-ae75-a11c40f318e2
title: TaskStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd74f25400093d9719607a718b4d1fc727ff36de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975021"
---
# <a name="systemcommunicationtaskstatus"></a><span data-ttu-id="ca99f-103">TaskStatus</span><span class="sxs-lookup"><span data-stu-id="ca99f-103">System.Communication.TaskStatus</span></span>

<span data-ttu-id="ca99f-104">表示工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ca99f-104">Indicates the current status of the task.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="ca99f-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="ca99f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotStarted
            value = 0
            text = Not Started
            defineToken = TASKSTATUS_NOTSTARTED
         enum
            name = InProgress
            value = 1
            text = In Progress
            defineToken = TASKSTATUS_INPROGRESS
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = TASKSTATUS_COMPLETE
         enum
            name = Waiting
            value = 3
            text = Waiting
            defineToken = TASKSTATUS_WAITING
         enum
            name = Deferred
            value = 4
            text = Deferred
            defineToken = TASKSTATUS_DEFERRED
```

## <a name="windows-vista"></a><span data-ttu-id="ca99f-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca99f-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not Started
            defineName = TASKSTATUS_NOTSTARTED
         enum
            value = 1
            text = In Progress
            defineName = TASKSTATUS_INPROGRESS
         enum
            value = 2
            text = Complete
            defineName = TASKSTATUS_COMPLETE
         enum
            value = 3
            text = Waiting
            defineName = TASKSTATUS_WAITING
         enum
            value = 4
            text = Deferred
            defineName = TASKSTATUS_DEFERRED
```

## <a name="remarks"></a><span data-ttu-id="ca99f-107">備註</span><span class="sxs-lookup"><span data-stu-id="ca99f-107">Remarks</span></span>

<span data-ttu-id="ca99f-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="ca99f-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca99f-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca99f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca99f-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ca99f-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ca99f-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ca99f-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ca99f-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ca99f-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ca99f-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ca99f-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ca99f-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ca99f-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ca99f-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ca99f-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ca99f-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ca99f-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ca99f-117">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="ca99f-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ca99f-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ca99f-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ca99f-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ca99f-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ca99f-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="ca99f-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ca99f-121">editControl</span><span class="sxs-lookup"><span data-stu-id="ca99f-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ca99f-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="ca99f-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ca99f-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="ca99f-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
