---
description: 這個屬性類似于 ItemNameDisplay，但它只會針對資料夾進行設定，而檔案將會是空的。
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980353"
---
# <a name="systemfoldernamedisplay"></a><span data-ttu-id="1ce39-103">System. FolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="1ce39-103">System.FolderNameDisplay</span></span>

<span data-ttu-id="1ce39-104">這個屬性類似于 ItemNameDisplay，但它只會針對資料夾進行設定，而檔案將會是空的。</span><span class="sxs-lookup"><span data-stu-id="1ce39-104">This property is similar to System.ItemNameDisplay except it is only set for folders, for files it will be empty.</span></span> <span data-ttu-id="1ce39-105">使用這個做為第一個排序索引鍵來分隔檔案和資料夾，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="1ce39-105">This is useful to segregate files and folders by using this as the first sort key.</span></span> <span data-ttu-id="1ce39-106">當使用 ItemDate 做為第二個排序索引鍵時，它會產生第一個依名稱排序的資料夾結果，然後依日期排序的檔案。</span><span class="sxs-lookup"><span data-stu-id="1ce39-106">When System.ItemDate is used as a second sort key it produces results with folders first ordered by name, then files ordered by date.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="1ce39-107">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="1ce39-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1ce39-108">備註</span><span class="sxs-lookup"><span data-stu-id="1ce39-108">Remarks</span></span>

<span data-ttu-id="1ce39-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="1ce39-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ce39-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ce39-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce39-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1ce39-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1ce39-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1ce39-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1ce39-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1ce39-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1ce39-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1ce39-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1ce39-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1ce39-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1ce39-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1ce39-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1ce39-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1ce39-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1ce39-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="1ce39-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1ce39-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1ce39-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1ce39-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1ce39-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1ce39-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="1ce39-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1ce39-122">editControl</span><span class="sxs-lookup"><span data-stu-id="1ce39-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1ce39-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="1ce39-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1ce39-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="1ce39-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
