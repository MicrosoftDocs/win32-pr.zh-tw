---
description: 檔案或媒體的取得日期。
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194831"
---
# <a name="systemdateacquired"></a><span data-ttu-id="a94dd-103">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="a94dd-103">System.DateAcquired</span></span>

<span data-ttu-id="a94dd-104">檔案或媒體的取得日期。</span><span class="sxs-lookup"><span data-stu-id="a94dd-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="a94dd-105">這個屬性與特定使用者或使用者群組有關。</span><span class="sxs-lookup"><span data-stu-id="a94dd-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="a94dd-106">例如，這項資料是用來做為虛擬資料夾 **新音樂** 的主要排序軸，可讓使用者流覽其集合的最新新增專案。</span><span class="sxs-lookup"><span data-stu-id="a94dd-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a94dd-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="a94dd-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="a94dd-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a94dd-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="a94dd-109">備註</span><span class="sxs-lookup"><span data-stu-id="a94dd-109">Remarks</span></span>

<span data-ttu-id="a94dd-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="a94dd-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="a94dd-111">[DateAcquired]() 會以值的形式儲存在檔案的主要資料流程中，但不一定會存在。</span><span class="sxs-lookup"><span data-stu-id="a94dd-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="a94dd-112">在這些情況下，取得日期可以根據其他已知的內容日期來近似值。</span><span class="sxs-lookup"><span data-stu-id="a94dd-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="a94dd-113">元資料處理程式應該使用一組規則來決定要傳回的日期。</span><span class="sxs-lookup"><span data-stu-id="a94dd-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="a94dd-114">下列範例示範音樂檔案的這項工作。</span><span class="sxs-lookup"><span data-stu-id="a94dd-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="a94dd-115">針對已購買的音樂，如果未取得任何日期，則應該使用檔案的建立時間。</span><span class="sxs-lookup"><span data-stu-id="a94dd-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="a94dd-116">不過，下載提供者應該在檔案中設定 [DateAcquired]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="a94dd-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="a94dd-117">若為使用者或群組「已翻錄」 (將音樂或影片從 CD 或 DVD 複製到硬碟) 的音樂檔案，則取得日期應該是動作發生的日期。</span><span class="sxs-lookup"><span data-stu-id="a94dd-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="a94dd-118">例如， [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a94dd-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="a94dd-119">若為從另一個位置複製的音樂，則應該使用檔案的建立時間做為取得日期。</span><span class="sxs-lookup"><span data-stu-id="a94dd-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="a94dd-120">[DateAcquired]()的範例是從相機取得圖片或在線上購買音樂時的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a94dd-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="a94dd-121">這與 [DateImported](./props-system-dateimported.md)不同。</span><span class="sxs-lookup"><span data-stu-id="a94dd-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a94dd-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="a94dd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94dd-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a94dd-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a94dd-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a94dd-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a94dd-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a94dd-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a94dd-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a94dd-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a94dd-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a94dd-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a94dd-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a94dd-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a94dd-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a94dd-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a94dd-130">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="a94dd-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a94dd-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a94dd-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a94dd-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a94dd-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a94dd-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="a94dd-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a94dd-134">editControl</span><span class="sxs-lookup"><span data-stu-id="a94dd-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a94dd-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="a94dd-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a94dd-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="a94dd-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
