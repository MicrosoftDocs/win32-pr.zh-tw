---
description: 此屬性代表存放裝置提供者所指定的檔案/資料夾最寬鬆的共用狀態。從最寬鬆到最低的共用狀態是擁有 > 共同擁有的 > Public > 共用 > 私用。 StorageProviderSharingStatus 是唯讀屬性。
ms.assetid: c3b93159-4279-4b27-b006-ab73e0beee9c
title: System. StorageProviderSharingStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b5b6b23b3a541037511eee3ae7201252e4ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971496"
---
# <a name="systemstorageprovidersharingstatus"></a><span data-ttu-id="9025f-103">System. StorageProviderSharingStatus</span><span class="sxs-lookup"><span data-stu-id="9025f-103">System.StorageProviderSharingStatus</span></span>

<span data-ttu-id="9025f-104">此屬性代表存放裝置提供者所指定的檔案/資料夾最寬鬆的共用狀態。從最寬鬆到最低的共用狀態是擁有 > 共同擁有的 > Public > 共用 > 私用。 StorageProviderSharingStatus 是唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="9025f-104">This property represents a the most permissive share status for the file/folder specified by the storage provider.The share statuses from most to least permissive are Owned > Co-owned > Public > Shared > Private.StorageProviderSharingStatus is a readonly property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="9025f-105">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="9025f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderSharingStatus
   shellPKey = PKEY_StorageProviderSharingStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 117
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PRIVATE
         enum
            name = Public
            value = 3
            text = Public
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC
         enum
            name = SharedOwned
            value = 4
            text = Shared (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_OWNED
         enum
            name = SharedCoOwned
            value = 5
            text = Shared (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_COOWNED
         enum
            name = PublicOwned
            value = 6
            text = Public (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_OWNED
         enum
            name = PublicCoOwned
            value = 7
            text = Public (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_COOWNED
```

## <a name="remarks"></a><span data-ttu-id="9025f-106">備註</span><span class="sxs-lookup"><span data-stu-id="9025f-106">Remarks</span></span>

<span data-ttu-id="9025f-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="9025f-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9025f-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="9025f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9025f-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9025f-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9025f-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9025f-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9025f-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9025f-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9025f-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9025f-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9025f-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9025f-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9025f-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9025f-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9025f-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9025f-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9025f-116">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="9025f-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9025f-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9025f-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9025f-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9025f-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9025f-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="9025f-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9025f-120">editControl</span><span class="sxs-lookup"><span data-stu-id="9025f-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9025f-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="9025f-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9025f-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="9025f-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
