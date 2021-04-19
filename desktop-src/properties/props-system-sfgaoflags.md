---
description: SFGAO IShellFolder：： GetAttributesOf 中所使用的值。
ms.assetid: 0a63e019-a03c-43c2-b2dc-20ef7c37e0d3
title: System. SFGAOFlags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71ced08bd2a3a916924ff876cadb160cf6fb959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975910"
---
# <a name="systemsfgaoflags"></a><span data-ttu-id="b3097-103">System. SFGAOFlags</span><span class="sxs-lookup"><span data-stu-id="b3097-103">System.SFGAOFlags</span></span>

<span data-ttu-id="b3097-104">[**SFGAO**](../shell/sfgao.md) [**IShellFolder：： GetAttributesOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)中所使用的值。</span><span class="sxs-lookup"><span data-stu-id="b3097-104">[**SFGAO**](../shell/sfgao.md) values as used in [**IShellFolder::GetAttributesOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="b3097-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="b3097-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.SFGAOFlags
   shellPKey = PKEY_SFGAOFlags
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="b3097-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3097-106">Windows Vista</span></span>

```
propertyDescription
   name = System.SFGAOFlags
   shellPKey = PKEY_SFGAOFlags
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 25
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="b3097-107">備註</span><span class="sxs-lookup"><span data-stu-id="b3097-107">Remarks</span></span>

<span data-ttu-id="b3097-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="b3097-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b3097-109">使用 [\* \* \* \* SFGAO \_ PKEYSFGAOMASK \* \*](../shell/sfgao.md) \* \* 遮罩的應用程式時，會將某些 [**SFGAO**](../shell/sfgao.md)值視為導致緩慢的計算或缺少內容。</span><span class="sxs-lookup"><span data-stu-id="b3097-109">Certain [**SFGAO**](../shell/sfgao.md) values that are considered to cause slow calculations or lack context are excluded here by the application of the [\*\*\*\*SFGAO\_PKEYSFGAOMASK\*\*\*\*](../shell/sfgao.md) mask.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3097-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3097-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3097-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b3097-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b3097-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b3097-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b3097-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b3097-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b3097-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b3097-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b3097-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b3097-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b3097-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b3097-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b3097-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b3097-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b3097-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="b3097-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b3097-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b3097-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b3097-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b3097-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b3097-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="b3097-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b3097-122">editControl</span><span class="sxs-lookup"><span data-stu-id="b3097-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b3097-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="b3097-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b3097-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="b3097-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
