---
title: 封裝、部署和查詢詞彙
description: 提供與封裝、部署及查詢 Windows apps 相關之詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a273b82806a724e50c7f29c512d19e1723283582abb3aa8b97f49f6293182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130270"
---
# <a name="packaging-deployment-and-query-glossary"></a>封裝、部署和查詢詞彙

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**應用程式使用者模型識別碼**
</dt> <dd>

應用程式使用者模型識別碼可唯一識別作業系統上的應用程式，讓作業系統可以將通知傳送至應用程式。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**區塊對應**
</dt> <dd>

針對儲存在應用程式封裝檔案中的可執行程式碼和資料，定義索引和密碼編譯雜湊。 每個應用程式封裝都需要 BlockMap.xml 檔。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**相依性套件**
</dt> <dd>

另一個封裝所相依的封裝。 相依性是在相依套件的資訊清單中宣告，而非相依性套件的資訊清單中。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**相依套件**
</dt> <dd>

對另一個套件具有相依性的套件。 相依性是在相依套件的資訊清單中宣告的。

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**使用量檔案**
</dt> <dd>

應用程式套件內的檔案不是要部署之應用程式的一部分。 這些檔案提供與封裝相關的中繼資料。 標準使用量檔案包含資訊清單、區塊對應、串流對應和數位簽章。 在封裝組建程式中會建立使用量檔案。 除了 OPC 規格之外，.xml 的 \[ 內容 \_ 類型 \] 和名稱符合 " \* \\ \_ .rels \\ \* . .rels" 模式的檔案都是磁片使用量檔案。

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**清單**
</dt> <dd>

描述與封裝相關聯之內容和中繼資料的 XML 檔案，包括封裝識別碼。 每個應用程式封裝都需要資訊清單 XML 檔案。

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

開放式封裝慣例 (OPC) 描述以 ISO/IEC 29500 和 ECMA 376 標準記載的容器檔案技術。 應用程式套件符合 OPC 規範。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**包**
</dt> <dd>

與應用程式封裝模型相關聯的部署、管理和服務軟體的單位。 套件包含構成應用程式的檔案，以及描述要 Windows 之軟體的資訊清單檔。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**套件系列名稱**
</dt> <dd>

封裝識別碼的序列化形式，可唯一代表電腦上的套件系列。 它適用于命名物件，例如檔案和資料夾。 套件系列名稱類似于封裝的完整名稱，但只包含名稱和發行者。 因為它會排除因服務 (版本、架構和資源資訊) 而變更的資訊，所以對於套件的版本獨立參考很有用。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**套件完整名稱**
</dt> <dd>

封裝識別碼的序列化形式，可在電腦上唯一表示此版本的封裝。 它適用于命名物件，例如檔案和資料夾。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**套件識別碼**
</dt> <dd>

封裝的全域唯一識別碼。 它是由封裝的屬性元組所組成，包括名稱、發行者、支援的架構、資源資訊和版本。 如需封裝識別碼的序列化形式，請參閱套件的完整名稱和套件系列名稱。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**套件相對應用程式識別碼**
</dt> <dd>

封裝資訊清單（也稱為 PRAID）中 [**應用程式**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application)元素的 **Id** 屬性。 這個字串可唯一識別封裝內的應用程式。 **應用程式** 元素需要這個屬性。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**承載檔**
</dt> <dd>

應用程式套件內的檔案，屬於要部署之應用程式的一部分。 這些檔案會解壓縮並放在使用者的安裝資料夾中。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**資源識別碼**
</dt> <dd>

封裝識別碼的選擇性部分，用來區別封裝中的資源。 例如，資源識別碼可以用來指定語言或地區設定。

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central 目錄**
</dt> <dd>

ZIP 檔案中的位元組序列，會儲存 ZIP 封存的相關中繼資料及其內容，包括名稱、大小、壓縮設定，以及封存內的位置。

</dd> </dl>

 

 