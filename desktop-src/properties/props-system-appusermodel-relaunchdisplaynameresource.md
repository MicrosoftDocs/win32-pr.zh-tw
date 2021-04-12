---
description: 指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的顯示名稱。
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192842"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="d810a-103">AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="d810a-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="d810a-104">指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d810a-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="d810a-105">這個屬性的值必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d810a-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="d810a-106">間接資源字串，例如 "@% systemdir% \\ system32 \\shell32.dll，-19263"。</span><span class="sxs-lookup"><span data-stu-id="d810a-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="d810a-107">請注意，必須有 ' @ ' 字元，才能區別純文字字串中的間接字串 (下一個點符段落) 所述。</span><span class="sxs-lookup"><span data-stu-id="d810a-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="d810a-108">這個間接字串是由二進位檔案和該二進位檔中所包含之字串的資源識別碼所組成。</span><span class="sxs-lookup"><span data-stu-id="d810a-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="d810a-109">強烈建議您使用這個間接字串表單，以確保當系統語言透過多語系消費者介面 (MUI) 變更時，顯示名稱會適當地變更。</span><span class="sxs-lookup"><span data-stu-id="d810a-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="d810a-110">需要資源識別碼之前的 '-' 字元。</span><span class="sxs-lookup"><span data-stu-id="d810a-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="d810a-111">未指向資源的純文字字串。</span><span class="sxs-lookup"><span data-stu-id="d810a-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="d810a-112">只有當顯示名稱是動態計算，或從不支援 MUI 的資料來源取得時，才應該使用此方法。</span><span class="sxs-lookup"><span data-stu-id="d810a-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="d810a-113">例如，如果應用程式在裝置連接到電腦時出現，則字串可能是裝置的名稱（例如 "Microsoft Zune"）。</span><span class="sxs-lookup"><span data-stu-id="d810a-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="d810a-114">[AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) 和 [AppUserModel. RelaunchDisplayNameResource]() 一律必須一起設定。</span><span class="sxs-lookup"><span data-stu-id="d810a-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="d810a-115">如果未設定其中一個屬性，則不會使用這兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="d810a-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="d810a-116">只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d810a-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="d810a-117">如果視窗沒有明確的 AppUserModelID，則會忽略此屬性，並將視窗分組並釘選，就好像它是擁有它的進程的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="d810a-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="d810a-118">如需明確 AppUserModelIDs 及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。</span><span class="sxs-lookup"><span data-stu-id="d810a-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="d810a-119">這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。</span><span class="sxs-lookup"><span data-stu-id="d810a-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="d810a-120">如需詳細資訊，請參閱 [AppUserModel。 RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)。</span><span class="sxs-lookup"><span data-stu-id="d810a-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="d810a-121">如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d810a-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="d810a-122">這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。</span><span class="sxs-lookup"><span data-stu-id="d810a-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="d810a-123">若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchDisplayNameResource]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="d810a-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="d810a-124">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="d810a-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="d810a-125">備註</span><span class="sxs-lookup"><span data-stu-id="d810a-125">Remarks</span></span>

<span data-ttu-id="d810a-126">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="d810a-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d810a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d810a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d810a-128">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="d810a-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="d810a-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="d810a-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="d810a-130">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="d810a-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="d810a-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d810a-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d810a-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d810a-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d810a-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d810a-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d810a-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-136">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="d810a-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d810a-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d810a-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d810a-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d810a-139">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="d810a-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d810a-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d810a-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d810a-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d810a-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d810a-142">枚舉</span><span class="sxs-lookup"><span data-stu-id="d810a-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="d810a-143">enumRange</span><span class="sxs-lookup"><span data-stu-id="d810a-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="d810a-144">image</span><span class="sxs-lookup"><span data-stu-id="d810a-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="d810a-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="d810a-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d810a-146">editControl</span><span class="sxs-lookup"><span data-stu-id="d810a-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d810a-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="d810a-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d810a-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="d810a-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="d810a-149">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="d810a-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="d810a-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="d810a-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
