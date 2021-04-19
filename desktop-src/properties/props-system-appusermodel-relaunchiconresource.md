---
description: 指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的圖示。
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980776"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="14b2a-103">AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="14b2a-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="14b2a-104">指定當使用者選擇將應用程式釘選到工作列或透過按鈕的捷徑清單啟動新實例時，在工作列上建立的快捷方式所使用的圖示。</span><span class="sxs-lookup"><span data-stu-id="14b2a-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="14b2a-105">這是用於工作列群組的圖示，會針對已釘選的應用程式顯示（無論應用程式是否正在執行）。</span><span class="sxs-lookup"><span data-stu-id="14b2a-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="14b2a-106">這應該以下列其中一種格式來指定：</span><span class="sxs-lookup"><span data-stu-id="14b2a-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="14b2a-107">標準資源格式，例如 "% systemdir% \\ system32 \\shell32.dll，-128"。</span><span class="sxs-lookup"><span data-stu-id="14b2a-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="14b2a-108">需要資源識別碼之前的 '-' 字元。</span><span class="sxs-lookup"><span data-stu-id="14b2a-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="14b2a-109">請勿在路徑字串的前方使用 ' @ ' 字元。</span><span class="sxs-lookup"><span data-stu-id="14b2a-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="14b2a-110">圖示檔的直接路徑，例如 "% programfiles% \\ Microsoft \\ notepad \\ notepad .ico，0"。</span><span class="sxs-lookup"><span data-stu-id="14b2a-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="14b2a-111">請注意，因為 .ico 檔案可以包含多個圖示資源，所以字串中必須有資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14b2a-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="14b2a-112">如果 .ico 檔案是單一映射，請使用 "0" (不含 '-' 字元) 作為資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14b2a-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="14b2a-113">[AppUserModel. RelaunchIconResource]() 是選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="14b2a-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="14b2a-114">如果未設定，則會使用重新開機命令的靶心圖表標 ([AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) 。</span><span class="sxs-lookup"><span data-stu-id="14b2a-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="14b2a-115">不過，因為這可能會導致不想要的結果，所以強烈建議您透過這個屬性明確提供圖示。</span><span class="sxs-lookup"><span data-stu-id="14b2a-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="14b2a-116">只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="14b2a-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="14b2a-117">如果視窗沒有明確的 AppUserModelID (System.AppUserModel.ID) ，則會忽略此屬性，並將視窗分組並釘選，就好像它是其擁有進程的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="14b2a-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="14b2a-118">如需明確 AppUserModelIDs 及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。</span><span class="sxs-lookup"><span data-stu-id="14b2a-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="14b2a-119">這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。</span><span class="sxs-lookup"><span data-stu-id="14b2a-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="14b2a-120">如需詳細資訊，請參閱 [AppUserModel。 RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)。</span><span class="sxs-lookup"><span data-stu-id="14b2a-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="14b2a-121">如果在視窗上設定了明確的 AppUserModelID，但是未設定此屬性，系統就會嘗試尋找具有相同 AppUserModelID 的快捷方式，並將快捷方式釘選到工作列以表示視窗。</span><span class="sxs-lookup"><span data-stu-id="14b2a-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="14b2a-122">如果找不到這種快捷方式，則會使用擁有它之進程的支援可執行檔。</span><span class="sxs-lookup"><span data-stu-id="14b2a-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="14b2a-123">如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="14b2a-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="14b2a-124">這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。</span><span class="sxs-lookup"><span data-stu-id="14b2a-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="14b2a-125">若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchIconResource]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="14b2a-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="14b2a-126">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="14b2a-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="14b2a-127">Windows 8，Windows 7</span><span class="sxs-lookup"><span data-stu-id="14b2a-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="14b2a-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="14b2a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b2a-129">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="14b2a-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="14b2a-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="14b2a-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="14b2a-131">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="14b2a-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="14b2a-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="14b2a-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="14b2a-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-137">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="14b2a-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="14b2a-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="14b2a-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="14b2a-140">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="14b2a-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="14b2a-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="14b2a-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="14b2a-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="14b2a-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="14b2a-143">枚舉</span><span class="sxs-lookup"><span data-stu-id="14b2a-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="14b2a-144">enumRange</span><span class="sxs-lookup"><span data-stu-id="14b2a-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="14b2a-145">image</span><span class="sxs-lookup"><span data-stu-id="14b2a-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="14b2a-146">drawControl</span><span class="sxs-lookup"><span data-stu-id="14b2a-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="14b2a-147">editControl</span><span class="sxs-lookup"><span data-stu-id="14b2a-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="14b2a-148">filterControl</span><span class="sxs-lookup"><span data-stu-id="14b2a-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="14b2a-149">queryControl</span><span class="sxs-lookup"><span data-stu-id="14b2a-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="14b2a-150">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="14b2a-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="14b2a-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="14b2a-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
