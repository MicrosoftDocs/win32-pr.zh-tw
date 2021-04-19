---
description: 指定可透過 ShellExecute 執行的命令，以在應用程式釘選到工作列時啟動應用程式，或透過應用程式的捷徑清單啟動應用程式的新實例。
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980777"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="87148-103">AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="87148-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="87148-104">指定可透過 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 執行的命令，以在應用程式釘選到工作列時啟動應用程式，或透過應用程式的捷徑清單啟動應用程式的新實例。</span><span class="sxs-lookup"><span data-stu-id="87148-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="87148-105">範例包括：</span><span class="sxs-lookup"><span data-stu-id="87148-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="87148-106">只有當視窗具有明確的應用程式使用者模型識別碼 (AppUserModelID)  ([System.AppUserModel.ID](./props-system-appusermodel-id.md)（透過 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) 設定）時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="87148-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="87148-107">如果視窗沒有明確的 AppUserModelID，則會忽略此屬性，並將視窗分組並釘選，就好像它是擁有它的進程的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="87148-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="87148-108">如需明確 AppUserModelIDs 的應用程式及其對工作列釘選效果的詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。</span><span class="sxs-lookup"><span data-stu-id="87148-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="87148-109">這個屬性的目的是要讓想要提供非預設重新開機資訊的應用程式或視窗使用。</span><span class="sxs-lookup"><span data-stu-id="87148-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="87148-110">[AppUserModel. RelaunchCommand]() 和 [AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) 一律必須一起設定。</span><span class="sxs-lookup"><span data-stu-id="87148-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="87148-111">如果未設定其中一個屬性，則不會使用這兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="87148-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="87148-112">這個屬性（property）連同 [AppUserModel （RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) ）和 [AppUserModel （RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) ）可用來以視覺方式將視窗定義為使用者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="87148-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="87148-113">這適用于裝載應用程式案例，其中單一主控制項實例會執行多個子應用程式。</span><span class="sxs-lookup"><span data-stu-id="87148-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="87148-114">例如，裝載數個虛擬化應用程式的虛擬機器可能會想要讓這些虛擬化應用程式以個別的應用程式顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="87148-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="87148-115">虛擬機器可以用明確的 AppUserModelID 和適當的重新開機屬性為每個視窗加上標籤，使其顯示為應用程式。</span><span class="sxs-lookup"><span data-stu-id="87148-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="87148-116">然後使用者可以將它們釘選到工作列，然後「重新開機」已釘選的實例。</span><span class="sxs-lookup"><span data-stu-id="87148-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="87148-117">如果設定了 [AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) ，就會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="87148-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="87148-118">這可讓應用程式藉由指派明確的 AppUserModelIDs 來控制其視窗的群組，但無法釘選這些視窗。</span><span class="sxs-lookup"><span data-stu-id="87148-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="87148-119">若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [AppUserModel. RelaunchCommand]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="87148-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="87148-120">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="87148-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="87148-121">備註</span><span class="sxs-lookup"><span data-stu-id="87148-121">Remarks</span></span>

<span data-ttu-id="87148-122">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="87148-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87148-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="87148-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87148-124">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="87148-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="87148-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="87148-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="87148-126">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="87148-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="87148-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="87148-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="87148-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="87148-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="87148-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="87148-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="87148-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-132">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="87148-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="87148-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="87148-134">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="87148-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="87148-135">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="87148-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="87148-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="87148-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="87148-137">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="87148-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="87148-138">枚舉</span><span class="sxs-lookup"><span data-stu-id="87148-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="87148-139">enumRange</span><span class="sxs-lookup"><span data-stu-id="87148-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="87148-140">image</span><span class="sxs-lookup"><span data-stu-id="87148-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="87148-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="87148-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="87148-142">editControl</span><span class="sxs-lookup"><span data-stu-id="87148-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="87148-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="87148-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="87148-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="87148-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="87148-145">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="87148-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="87148-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="87148-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
