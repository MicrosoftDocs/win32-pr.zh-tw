---
title: 封裝、部署和查詢詞彙
description: 提供 Windows 應用程式封裝、部署和查詢相關詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104374952"
---
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="76cc9-103">封裝、部署和查詢詞彙</span><span class="sxs-lookup"><span data-stu-id="76cc9-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="76cc9-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**應用程式使用者模型識別碼**</span><span class="sxs-lookup"><span data-stu-id="76cc9-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-105">應用程式使用者模型識別碼可唯一識別作業系統上的應用程式，讓作業系統可以將通知傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="76cc9-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**區塊對應**</span><span class="sxs-lookup"><span data-stu-id="76cc9-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-107">針對儲存在應用程式封裝檔案中的可執行程式碼和資料，定義索引和密碼編譯雜湊。</span><span class="sxs-lookup"><span data-stu-id="76cc9-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="76cc9-108">每個應用程式封裝都需要 BlockMap.xml 檔。</span><span class="sxs-lookup"><span data-stu-id="76cc9-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**相依性套件**</span><span class="sxs-lookup"><span data-stu-id="76cc9-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-110">另一個封裝所相依的封裝。</span><span class="sxs-lookup"><span data-stu-id="76cc9-110">A package on which another package depends.</span></span> <span data-ttu-id="76cc9-111">相依性是在相依套件的資訊清單中宣告，而非相依性套件的資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="76cc9-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**相依套件**</span><span class="sxs-lookup"><span data-stu-id="76cc9-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-113">對另一個套件具有相依性的套件。</span><span class="sxs-lookup"><span data-stu-id="76cc9-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="76cc9-114">相依性是在相依套件的資訊清單中宣告的。</span><span class="sxs-lookup"><span data-stu-id="76cc9-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**使用量檔案**</span><span class="sxs-lookup"><span data-stu-id="76cc9-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-116">應用程式套件內的檔案不是要部署之應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="76cc9-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="76cc9-117">這些檔案提供與封裝相關的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="76cc9-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="76cc9-118">標準使用量檔案包含資訊清單、區塊對應、串流對應和數位簽章。</span><span class="sxs-lookup"><span data-stu-id="76cc9-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="76cc9-119">在封裝組建程式中會建立使用量檔案。</span><span class="sxs-lookup"><span data-stu-id="76cc9-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="76cc9-120">此外，根據 OPC 規格， \[ 內容 \_ 類型 \] .xml 和名稱符合 " \* \\ \_ .rels \\ \* . .rels" 模式的檔案都是磁片使用量檔案。</span><span class="sxs-lookup"><span data-stu-id="76cc9-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**清單**</span><span class="sxs-lookup"><span data-stu-id="76cc9-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-122">描述與封裝相關聯之內容和中繼資料的 XML 檔案，包括封裝識別碼。</span><span class="sxs-lookup"><span data-stu-id="76cc9-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="76cc9-123">每個應用程式封裝都需要資訊清單 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="76cc9-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**Opc**</span><span class="sxs-lookup"><span data-stu-id="76cc9-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-125">開放式封裝慣例 (OPC) 描述以 ISO/IEC 29500 和 ECMA 376 標準記載的容器檔案技術。</span><span class="sxs-lookup"><span data-stu-id="76cc9-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="76cc9-126">應用程式套件符合 OPC 規範。</span><span class="sxs-lookup"><span data-stu-id="76cc9-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**包**</span><span class="sxs-lookup"><span data-stu-id="76cc9-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-128">與應用程式封裝模型相關聯的部署、管理和服務軟體的單位。</span><span class="sxs-lookup"><span data-stu-id="76cc9-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="76cc9-129">套件包含構成應用程式的檔案，以及描述軟體至 Windows 的資訊清單檔案。</span><span class="sxs-lookup"><span data-stu-id="76cc9-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**套件系列名稱**</span><span class="sxs-lookup"><span data-stu-id="76cc9-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-131">封裝識別碼的序列化形式，可唯一代表電腦上的套件系列。</span><span class="sxs-lookup"><span data-stu-id="76cc9-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="76cc9-132">它適用于命名物件，例如檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="76cc9-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="76cc9-133">套件系列名稱類似于封裝的完整名稱，但只包含名稱和發行者。</span><span class="sxs-lookup"><span data-stu-id="76cc9-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="76cc9-134">因為它會排除因服務 (版本、架構和資源資訊) 而變更的資訊，所以對於套件的版本獨立參考很有用。</span><span class="sxs-lookup"><span data-stu-id="76cc9-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**套件完整名稱**</span><span class="sxs-lookup"><span data-stu-id="76cc9-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-136">封裝識別碼的序列化形式，可在電腦上唯一表示此版本的封裝。</span><span class="sxs-lookup"><span data-stu-id="76cc9-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="76cc9-137">它適用于命名物件，例如檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="76cc9-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**套件識別碼**</span><span class="sxs-lookup"><span data-stu-id="76cc9-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-139">封裝的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="76cc9-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="76cc9-140">它是由封裝的屬性元組所組成，包括名稱、發行者、支援的架構、資源資訊和版本。</span><span class="sxs-lookup"><span data-stu-id="76cc9-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="76cc9-141">如需封裝識別碼的序列化形式，請參閱套件的完整名稱和套件系列名稱。</span><span class="sxs-lookup"><span data-stu-id="76cc9-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**套件相對應用程式識別碼**</span><span class="sxs-lookup"><span data-stu-id="76cc9-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-143">封裝資訊清單（也稱為 PRAID）中 [**應用程式**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application)元素的 **Id** 屬性。</span><span class="sxs-lookup"><span data-stu-id="76cc9-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="76cc9-144">這個字串可唯一識別封裝內的應用程式。</span><span class="sxs-lookup"><span data-stu-id="76cc9-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="76cc9-145">**應用程式** 元素需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="76cc9-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**承載檔**</span><span class="sxs-lookup"><span data-stu-id="76cc9-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-147">應用程式套件內的檔案，屬於要部署之應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="76cc9-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="76cc9-148">這些檔案會解壓縮並放在使用者的安裝資料夾中。</span><span class="sxs-lookup"><span data-stu-id="76cc9-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**資源識別碼**</span><span class="sxs-lookup"><span data-stu-id="76cc9-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-150">封裝識別碼的選擇性部分，用來區別封裝中的資源。</span><span class="sxs-lookup"><span data-stu-id="76cc9-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="76cc9-151">例如，資源識別碼可以用來指定語言或地區設定。</span><span class="sxs-lookup"><span data-stu-id="76cc9-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="76cc9-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central 目錄**</span><span class="sxs-lookup"><span data-stu-id="76cc9-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="76cc9-153">ZIP 檔案中的位元組序列，會儲存 ZIP 封存的相關中繼資料及其內容，包括名稱、大小、壓縮設定，以及封存內的位置。</span><span class="sxs-lookup"><span data-stu-id="76cc9-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 