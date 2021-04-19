---
description: 項目的標題。
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981207"
---
# <a name="systemtitle"></a><span data-ttu-id="6bf03-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="6bf03-103">System.Title</span></span>

<span data-ttu-id="6bf03-104">項目的標題。</span><span class="sxs-lookup"><span data-stu-id="6bf03-104">The title of the item.</span></span> <span data-ttu-id="6bf03-105">例如文件的標題、郵件的主旨、相片的標題或音樂曲目的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bf03-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6bf03-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="6bf03-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="6bf03-107">備註</span><span class="sxs-lookup"><span data-stu-id="6bf03-107">Remarks</span></span>

<span data-ttu-id="6bf03-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="6bf03-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6bf03-109">這個屬性會對應至 OLE 文件屬性 *標題*。</span><span class="sxs-lookup"><span data-stu-id="6bf03-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="6bf03-110">[System. Title]() 是常用的屬性，特別是在不同的專案清單中，這些專案的專案可以是許多不同的類型。</span><span class="sxs-lookup"><span data-stu-id="6bf03-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="6bf03-111">因此，即使屬性處理常式是多餘的，還是建議您填入此屬性。例如，電子郵件會將相同的值填入 System. Title 和[system。](./props-system-subject.md)</span><span class="sxs-lookup"><span data-stu-id="6bf03-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bf03-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bf03-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf03-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6bf03-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6bf03-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6bf03-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6bf03-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6bf03-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6bf03-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6bf03-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6bf03-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6bf03-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6bf03-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6bf03-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6bf03-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6bf03-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6bf03-120">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="6bf03-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6bf03-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6bf03-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6bf03-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6bf03-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6bf03-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="6bf03-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6bf03-124">editControl</span><span class="sxs-lookup"><span data-stu-id="6bf03-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6bf03-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="6bf03-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6bf03-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="6bf03-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
