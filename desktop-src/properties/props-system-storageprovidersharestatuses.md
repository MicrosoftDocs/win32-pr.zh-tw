---
description: 此屬性代表存放裝置提供者所指定之檔案/資料夾的共用狀態清單。每個共用狀態都必須是 [列舉 belowStorageProviderShareStatuses] 所指定的已知值之一，它只應由儲存提供者更新。
ms.assetid: 131bf48a-0ab9-4b1f-9625-6fca5d15219f
title: System. StorageProviderShareStatuses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92340e4afb1005146a32d2505292a5e60dec971
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987671"
---
# <a name="systemstorageprovidersharestatuses"></a><span data-ttu-id="607dd-103">System. StorageProviderShareStatuses</span><span class="sxs-lookup"><span data-stu-id="607dd-103">System.StorageProviderShareStatuses</span></span>

<span data-ttu-id="607dd-104">此屬性代表存放裝置提供者所指定之檔案/資料夾的共用狀態清單。每個共用狀態都必須是 [列舉 belowStorageProviderShareStatuses] 所指定的已知值之一，它只應由儲存提供者更新。</span><span class="sxs-lookup"><span data-stu-id="607dd-104">This property represents a list of share statuses for the file/folder specified by the storage provider.Each share status must be one of the known value specified by the enumerations belowStorageProviderShareStatuses is a readonly property, it should only be updated by the storage provider.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="607dd-105">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="607dd-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderShareStatuses
   shellPKey = PKEY_StorageProviderShareStatuses
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 111
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Private
            value = Private
            text = Private
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PRIVATE
            mnemonics = private
         enum
            name = Shared
            value = Shared
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_SHARED
            mnemonics = shared
         enum
            name = Public
            value = Public
            text = Public
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PUBLIC
            mnemonics = public
         enum
            name = Group
            value = Group
            text = Group
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_GROUP
            mnemonics = group
         enum
            name = Owner
            value = Owner
            text = Owner
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_OWNER
            mnemonics = owner
```

## <a name="remarks"></a><span data-ttu-id="607dd-106">備註</span><span class="sxs-lookup"><span data-stu-id="607dd-106">Remarks</span></span>

<span data-ttu-id="607dd-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="607dd-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="607dd-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="607dd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="607dd-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="607dd-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="607dd-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="607dd-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="607dd-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="607dd-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="607dd-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="607dd-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="607dd-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="607dd-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="607dd-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="607dd-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="607dd-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="607dd-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="607dd-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="607dd-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="607dd-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="607dd-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="607dd-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="607dd-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="607dd-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="607dd-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="607dd-120">editControl</span><span class="sxs-lookup"><span data-stu-id="607dd-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="607dd-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="607dd-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="607dd-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="607dd-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
