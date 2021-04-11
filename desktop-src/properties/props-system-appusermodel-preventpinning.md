---
description: 停用快速鍵或視窗釘選到工作列或 [開始] 功能表的能力。 這個屬性也會讓專案不符合 [開始] 功能表最常使用的 (MFU) 清單。
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849514"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="e42cc-104">AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="e42cc-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="e42cc-105">停用快速鍵或視窗釘選到工作列或 [ **開始** ] 功能表的能力。</span><span class="sxs-lookup"><span data-stu-id="e42cc-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="e42cc-106">這個屬性也會讓專案不符合 [ **開始** ] 功能表最常使用的 (MFU) 清單中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="e42cc-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="e42cc-107">您必須在 [PKEY \_ AppUserModel \_ ID](./props-system-appusermodel-id.md) 屬性之前的視窗上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e42cc-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="e42cc-108">\_設定 PKEY AppUserModel \_ ID 屬性之後，會忽略[PKEY \_ AppUserModel \_ PreventPinning]()的變更。</span><span class="sxs-lookup"><span data-stu-id="e42cc-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="e42cc-109">如需應用程式使用者模型識別碼的詳細資訊 (AppUserModelIDs) 和其他排除專案的方法不會釘選到工作列，也可以從 MFU 包含，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。</span><span class="sxs-lookup"><span data-stu-id="e42cc-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="e42cc-110">若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. PreventPinning]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="e42cc-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="e42cc-111">設定這個屬性會忽略下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e42cc-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="e42cc-112">AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="e42cc-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="e42cc-113">AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="e42cc-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="e42cc-114">AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="e42cc-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e42cc-115">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="e42cc-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="e42cc-116">備註</span><span class="sxs-lookup"><span data-stu-id="e42cc-116">Remarks</span></span>

<span data-ttu-id="e42cc-117">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="e42cc-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e42cc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e42cc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e42cc-119">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="e42cc-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="e42cc-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="e42cc-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="e42cc-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="e42cc-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="e42cc-122">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="e42cc-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="e42cc-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e42cc-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e42cc-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-128">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e42cc-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e42cc-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e42cc-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e42cc-131">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="e42cc-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e42cc-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e42cc-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e42cc-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e42cc-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e42cc-134">枚舉</span><span class="sxs-lookup"><span data-stu-id="e42cc-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="e42cc-135">enumRange</span><span class="sxs-lookup"><span data-stu-id="e42cc-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="e42cc-136">image</span><span class="sxs-lookup"><span data-stu-id="e42cc-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="e42cc-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="e42cc-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e42cc-138">editControl</span><span class="sxs-lookup"><span data-stu-id="e42cc-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e42cc-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="e42cc-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e42cc-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="e42cc-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="e42cc-141">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="e42cc-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e42cc-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="e42cc-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
