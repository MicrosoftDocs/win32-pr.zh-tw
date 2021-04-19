---
title: Install 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Install 元素會指定 Windows Media Player 用來安裝線上商店的值。
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Install 元素 Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981102"
---
# <a name="install-element"></a><span data-ttu-id="97850-106">Install 元素</span><span class="sxs-lookup"><span data-stu-id="97850-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="97850-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="97850-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="97850-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="97850-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="97850-109">**Install** 元素會指定 Windows Media Player 用來安裝線上商店的值。</span><span class="sxs-lookup"><span data-stu-id="97850-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="97850-110">屬性</span><span class="sxs-lookup"><span data-stu-id="97850-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="97850-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="97850-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="97850-112">副檔名為 .txt 之檔案的完整 URL，Windows Media Player 用來顯示使用者授權合約 (EULA) 。</span><span class="sxs-lookup"><span data-stu-id="97850-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="97850-113">這個檔案必須以 ANSI 格式編碼。</span><span class="sxs-lookup"><span data-stu-id="97850-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="97850-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="97850-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="97850-115">封裝的完整 URL （副檔名為 .cab），可用來安裝線上存放區。</span><span class="sxs-lookup"><span data-stu-id="97850-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="97850-116">封裝和封裝中的所有程式碼模組都必須經過簽署。</span><span class="sxs-lookup"><span data-stu-id="97850-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="97850-117">如需程式碼簽署的詳細資訊，請參閱 MSDN Library 中的程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="97850-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="97850-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="97850-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="97850-119">網頁的完整 URL，包含線上商店的隱私權原則資訊。</span><span class="sxs-lookup"><span data-stu-id="97850-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="97850-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (必要) </span><span class="sxs-lookup"><span data-stu-id="97850-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="97850-121">要執行之 EXE 或 INF 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="97850-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="97850-122">這個檔案必須包含在 **CodeURL** 屬性所指定的 CAB 檔案中。</span><span class="sxs-lookup"><span data-stu-id="97850-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="97850-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (選用) </span><span class="sxs-lookup"><span data-stu-id="97850-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="97850-124">傳遞給 **InstallApp** 屬性所指定之應用程式的命令列字串。</span><span class="sxs-lookup"><span data-stu-id="97850-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="97850-125">只有當 **InstallApp** 的值指定可執行檔時，才適用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="97850-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="97850-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>類型1所需的 **CatalogURL** (，已忽略類型 2) </span><span class="sxs-lookup"><span data-stu-id="97850-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="97850-127">線上商店編譯目錄的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="97850-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="97850-128">父/子項目</span><span class="sxs-lookup"><span data-stu-id="97850-128">Parent/Child Elements</span></span>



| <span data-ttu-id="97850-129">階層</span><span class="sxs-lookup"><span data-stu-id="97850-129">Hierarchy</span></span>       | <span data-ttu-id="97850-130">元素</span><span class="sxs-lookup"><span data-stu-id="97850-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="97850-131">父元素</span><span class="sxs-lookup"><span data-stu-id="97850-131">Parent elements</span></span> | <span data-ttu-id="97850-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="97850-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="97850-133">子元素</span><span class="sxs-lookup"><span data-stu-id="97850-133">Child elements</span></span>  | <span data-ttu-id="97850-134">無</span><span class="sxs-lookup"><span data-stu-id="97850-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="97850-135">備註</span><span class="sxs-lookup"><span data-stu-id="97850-135">Remarks</span></span>

<span data-ttu-id="97850-136">如果任何必要的屬性遺失或無法使用，Windows Media Player 安裝程式將不會嘗試下載並安裝線上商店提供者程式碼。</span><span class="sxs-lookup"><span data-stu-id="97850-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="97850-137">安裝程式將會設定 **ServiceInfo** 檔中所指定的離線預設值。</span><span class="sxs-lookup"><span data-stu-id="97850-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="97850-138">**ServiceInfo** 可在未連線至網際網路的情況下使用，方法是將預設提供者名稱和 **ServiceInfo** 資訊當做命令列參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="97850-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="97850-139">如需命令列選項的詳細資訊，請參閱轉散發 [Windows Media Player 軟體](redistributing-windows-media-player-software.md) 。</span><span class="sxs-lookup"><span data-stu-id="97850-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="97850-140">使用此專案時，您需要簽署與 Microsoft 的轉散發合約。</span><span class="sxs-lookup"><span data-stu-id="97850-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="97850-141">如需詳細資料，請洽詢您的業務代表。</span><span class="sxs-lookup"><span data-stu-id="97850-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97850-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="97850-142">Requirements</span></span>



| <span data-ttu-id="97850-143">需求</span><span class="sxs-lookup"><span data-stu-id="97850-143">Requirement</span></span> | <span data-ttu-id="97850-144">值</span><span class="sxs-lookup"><span data-stu-id="97850-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="97850-145">版本</span><span class="sxs-lookup"><span data-stu-id="97850-145">Version</span></span><br/> | <span data-ttu-id="97850-146">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="97850-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97850-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97850-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97850-148">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="97850-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="97850-149">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="97850-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="97850-150">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="97850-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

