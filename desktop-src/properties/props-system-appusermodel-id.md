---
description: 明確的應用程式使用者模型識別碼 (AppUserModelID) 用來將處理常式、檔案和視窗與特定應用程式產生關聯。
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318888"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="983b9-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="983b9-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="983b9-104">明確的應用程式使用者模型識別碼 (AppUserModelID) 用來將處理常式、檔案和視窗與特定應用程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="983b9-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="983b9-105">在某些情況下，就足以依賴系統指派給進程的內部 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="983b9-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="983b9-106">不過，擁有多個處理常式或在主機進程中執行之應用程式的應用程式，可能需要透過這個屬性明確地識別其本身，讓它可以在單一工作列按鈕下將它的其他不同視窗分組，並控制該應用程式捷徑清單的內容。</span><span class="sxs-lookup"><span data-stu-id="983b9-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="983b9-107">若要在視窗上設定此屬性，請使用 [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) 抓取視窗的屬性存放區，然後使用該抓取 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件的方法來設定該視窗的 [System.AppUserModel.ID]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="983b9-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="983b9-108">如需詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](../shell/appids.md)。</span><span class="sxs-lookup"><span data-stu-id="983b9-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="983b9-109">當設定 [System.AppUserModel.ID]() 屬性時，系統會通知工作列在提供的視窗或快捷方式上重新整理其資訊。</span><span class="sxs-lookup"><span data-stu-id="983b9-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="983b9-110">其他視窗和快速鍵屬性可以搭配明確的 AppUserModelID 使用，以進一步控制與視窗相關聯的群組和釘選、工作列中所用的顯示名稱和圖示，以及用來啟動釘選到工作列的應用程式，或透過該應用程式的捷徑清單的新應用程式實例的命令。</span><span class="sxs-lookup"><span data-stu-id="983b9-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="983b9-111">您應該先設定這些屬性，然後再設定 [System.AppUserModel.ID]() 屬性。</span><span class="sxs-lookup"><span data-stu-id="983b9-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="983b9-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="983b9-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="983b9-113">AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="983b9-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="983b9-114">AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="983b9-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="983b9-115">AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="983b9-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="983b9-116">AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="983b9-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="983b9-117">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="983b9-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="983b9-118">備註</span><span class="sxs-lookup"><span data-stu-id="983b9-118">Remarks</span></span>

<span data-ttu-id="983b9-119">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="983b9-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="983b9-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="983b9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="983b9-121">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="983b9-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="983b9-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="983b9-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="983b9-123">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="983b9-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="983b9-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="983b9-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="983b9-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="983b9-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="983b9-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="983b9-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="983b9-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-129">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="983b9-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="983b9-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="983b9-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="983b9-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="983b9-132">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="983b9-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="983b9-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="983b9-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="983b9-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="983b9-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="983b9-135">枚舉</span><span class="sxs-lookup"><span data-stu-id="983b9-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="983b9-136">enumRange</span><span class="sxs-lookup"><span data-stu-id="983b9-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="983b9-137">image</span><span class="sxs-lookup"><span data-stu-id="983b9-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="983b9-138">drawControl</span><span class="sxs-lookup"><span data-stu-id="983b9-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="983b9-139">editControl</span><span class="sxs-lookup"><span data-stu-id="983b9-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="983b9-140">filterControl</span><span class="sxs-lookup"><span data-stu-id="983b9-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="983b9-141">queryControl</span><span class="sxs-lookup"><span data-stu-id="983b9-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="983b9-142">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="983b9-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="983b9-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="983b9-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
