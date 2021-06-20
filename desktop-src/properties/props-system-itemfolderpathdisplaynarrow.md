---
description: 閱讀 ItemFolderPathDisplayNarrow 屬性，其代表專案之父資料夾的使用者易記顯示路徑。
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System. ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbee8a45eb6ea557e99c854464c7dc09ec5613d2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403911"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="36080-103">System. ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="36080-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="36080-104">專案之父資料夾的使用者易記顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="36080-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="36080-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="36080-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="36080-106">備註</span><span class="sxs-lookup"><span data-stu-id="36080-106">Remarks</span></span>

<span data-ttu-id="36080-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="36080-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="36080-108">字串的格式應該經過量身打造，讓資料夾名稱先出現，以針對窄的視圖資料行進行優化。</span><span class="sxs-lookup"><span data-stu-id="36080-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="36080-109">如果資料夾是檔案資料夾，則值會包含任何當地語系化的名稱。</span><span class="sxs-lookup"><span data-stu-id="36080-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="36080-110">如果 [ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) 是 VT \_ 空白，則此屬性也應為空白。</span><span class="sxs-lookup"><span data-stu-id="36080-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="36080-111">否則，應該由 ItemFolderPathDisplay 中的資料來源適當地衍生。</span><span class="sxs-lookup"><span data-stu-id="36080-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36080-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="36080-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36080-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="36080-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="36080-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="36080-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="36080-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="36080-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="36080-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="36080-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="36080-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="36080-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="36080-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="36080-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="36080-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="36080-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="36080-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="36080-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="36080-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="36080-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="36080-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="36080-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="36080-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="36080-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="36080-124">editControl</span><span class="sxs-lookup"><span data-stu-id="36080-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="36080-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="36080-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="36080-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="36080-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
