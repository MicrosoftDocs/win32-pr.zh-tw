---
title: 封裝查詢 API
description: 瞭解套件查詢 API，您可以使用它來取得系統上所安裝之應用程式套件的相關資訊。 每個應用程式套件都包含構成 Windows 應用程式的檔案，以及描述軟體至 Windows 的資訊清單檔案。
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023301"
---
# <a name="package-query-api"></a>封裝查詢 API

瞭解套件查詢 API，您可以使用它來取得系統上所安裝之應用程式套件的相關資訊。 每個應用程式套件都包含構成 Windows 應用程式的檔案，以及描述軟體至 Windows 的資訊清單檔案。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                 | 描述                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | 關閉所指定封裝資訊的參考。<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | 尋找目前使用者具有指定系列名稱的封裝。 <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | 從套件系列名稱和套件相對應用程式識別碼（ (PRAID) ）中，建立 [應用程式使用者模型識別碼](appx-packaging-glossary.md) 。 <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | 取得指定進程的 [應用程式使用者模型識別碼](appx-packaging-glossary.md) 。<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | 取得指定之標記的 [應用程式使用者模型識別碼](appx-packaging-glossary.md) 。<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | 取得目前進程的 [應用程式使用者模型識別碼](appx-packaging-glossary.md) 。<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | 取得呼叫進程的套件系列名稱。<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | 取得呼叫進程的封裝完整名稱。<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | 取得呼叫進程 (識別碼) 的封裝識別碼。<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | 取得呼叫進程的封裝資訊。<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | 取得呼叫進程的封裝資訊，以及指定封裝資料夾類型的選項。<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | 取得呼叫進程的封裝路徑。<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | 取得呼叫進程的封裝路徑，以及指定封裝資料夾類型的選項。<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | 取得指定封裝中應用程式的識別碼。<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | 取得指定進程的套件系列名稱。<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | 取得指定之標記的套件系列名稱。<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | 取得指定進程的封裝完整名稱。<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | 取得指定之標記的封裝完整名稱。<br/>                                                                                                   |
| [**GetPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | 取得指定進程 (識別碼) 的封裝識別碼。<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | 取得指定封裝的封裝資訊。<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | 取得指定封裝的封裝資訊，以及指定封裝資料夾類型的選項。<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | 取得指定封裝的路徑。<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | 取得指定封裝的路徑。<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | 取得指定封裝的路徑，以及指定封裝資料夾類型的選項。<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | 取得目前使用者具有指定系列名稱的封裝。 <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | 取得指定封裝的來源。<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | 取得指定之暫存封裝的路徑。<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | 取得指定之暫存封裝的路徑，以及指定封裝資料夾類型的選項。<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | 開啟指定封裝的封裝資訊。<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | 取得指定套件完整名稱的套件系列名稱。<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | 取得指定封裝識別碼的套件系列名稱。<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | 取得指定封裝識別碼 (識別碼) 的封裝完整名稱。<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | 取得指定套件完整名稱的封裝識別碼 (識別碼) 。<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | 取得指定套件系列名稱的封裝名稱和發行者識別碼 (識別碼) 。<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | 將 [應用程式使用者模型識別碼](appx-packaging-glossary.md) 解構為到其套件系列名稱和套件相對應用程式識別碼 (PRAID) 。<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | 指定封裝的來源。 <br/>                                                                                                                   |
| [**身分識別常數**](identity-constants.md)<br/>                                           | 指定封裝之識別欄位的字串長度。<br/>                                                                                |
| [**封裝常數**](package-constants.md)<br/>                                             | 指定如何處理封裝。<br/>                                                                                                           |
| [**套件 \_ 識別碼**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | 表示套件識別資訊，例如名稱、版本和發行者。<br/>                                                                  |
| [**封裝 \_ 資訊**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | 表示套件識別資訊，其中包含套件識別碼、完整名稱和安裝位置。<br/>                                  |
| [**套件 \_ 版本**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | 代表封裝版本資訊。<br/>                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[詞彙](appx-packaging-glossary.md)
</dt> <dt>

**參考**
</dt> <dt>

[應用程式套件資訊清單結構描述](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[封裝 API](interfaces.md)
</dt> <dt>

[套件部署 API](package-deployment-api.md)
</dt> </dl>

 

