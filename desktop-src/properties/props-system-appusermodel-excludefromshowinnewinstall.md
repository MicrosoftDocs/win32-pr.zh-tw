---
description: 防止新安裝的應用程式快捷方式 [開始] 功能表專案收到醒目提示。
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: AppUserModel. ExcludeFromShowInNewInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206cbbc6b07b0d3fec5833c046d4cb44c1e5e4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989429"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a><span data-ttu-id="7b5c4-103">AppUserModel. ExcludeFromShowInNewInstall</span><span class="sxs-lookup"><span data-stu-id="7b5c4-103">System.AppUserModel.ExcludeFromShowInNewInstall</span></span>

<span data-ttu-id="7b5c4-104">防止新安裝的應用程式快捷方式的 [ **開始** ] 功能表項目收到醒目提示。</span><span class="sxs-lookup"><span data-stu-id="7b5c4-104">Prevents a **Start** menu entry for a newly installed application shortcut from receiving a highlight.</span></span> <span data-ttu-id="7b5c4-105">這相當於在個別專案上，清除 [**自訂開始] 功能表** 視窗中的 [**反白顯示新安裝的程式**] 選項。</span><span class="sxs-lookup"><span data-stu-id="7b5c4-105">This is equivalent to clearing the **Highlight newly installed programs** option in the **Customize Start Menu** window on an individual item.</span></span> <span data-ttu-id="7b5c4-106">您應該在工具和次要應用程式的快捷方式上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="7b5c4-106">This property should be set on shortcuts for tools and secondary applications.</span></span>

> [!Note]  
> <span data-ttu-id="7b5c4-107">只有 Windows Vista 和 Windows 7 上的 [開始] 功能表才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7b5c4-107">This property is property is only used by the Start menu on Windows Vista and Windows 7.</span></span> <span data-ttu-id="7b5c4-108">Windows 8 和更新版本上的開始畫面或 [開始] 功能表不會使用屬性</span><span class="sxs-lookup"><span data-stu-id="7b5c4-108">The property is not used by the Start screen or Start menu on Windows 8 and later</span></span>

 

<span data-ttu-id="7b5c4-109">.</span><span class="sxs-lookup"><span data-stu-id="7b5c4-109">.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="7b5c4-110">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="7b5c4-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="7b5c4-111">備註</span><span class="sxs-lookup"><span data-stu-id="7b5c4-111">Remarks</span></span>

<span data-ttu-id="7b5c4-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="7b5c4-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b5c4-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b5c4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b5c4-114">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="7b5c4-114">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-115">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="7b5c4-115">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-116">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="7b5c4-116">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="7b5c4-117">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="7b5c4-117">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-118">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7b5c4-118">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-119">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-119">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-120">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-120">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-121">typeInfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-121">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-122">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-122">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-123">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-123">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7b5c4-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7b5c4-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-126">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="7b5c4-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7b5c4-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7b5c4-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-129">枚舉</span><span class="sxs-lookup"><span data-stu-id="7b5c4-129">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-130">enumRange</span><span class="sxs-lookup"><span data-stu-id="7b5c4-130">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-131">image</span><span class="sxs-lookup"><span data-stu-id="7b5c4-131">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-132">drawControl</span><span class="sxs-lookup"><span data-stu-id="7b5c4-132">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-133">editControl</span><span class="sxs-lookup"><span data-stu-id="7b5c4-133">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-134">filterControl</span><span class="sxs-lookup"><span data-stu-id="7b5c4-134">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-135">queryControl</span><span class="sxs-lookup"><span data-stu-id="7b5c4-135">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-136">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="7b5c4-136">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="7b5c4-137">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="7b5c4-137">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> <dt>

<span data-ttu-id="7b5c4-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b5c4-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span></span>
</dt> </dl>

 

 
