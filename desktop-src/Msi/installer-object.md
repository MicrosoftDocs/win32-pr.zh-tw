---
description: 最初必須建立安裝程式物件，以載入 COM 存取安裝程式函數所需的自動化支援。 這個物件會提供包裝函式來建立最上層的物件，並存取其方法。
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: 安裝程式物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998694"
---
# <a name="installer-object"></a>安裝程式物件

最初必須建立 **安裝程式** 物件，以載入 COM 存取安裝程式函數所需的自動化支援。 這個物件會提供包裝函式來建立最上層的物件，並存取其方法。

您可以從 ProgId "WindowsInstaller. Installer" 建立 **安裝程式** 物件。

## <a name="members"></a>成員

**安裝程式** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**安裝程式** 物件有這些方法。



| 方法                                                                   | 描述                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | 將來源新增至 sourcelist 中有效網路來源的清單。<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | 通告安裝套件。<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | 通告安裝套件。 <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | 將一或多個修補程式套用至有資格接收修補程式的產品。 將 [**patch**](patch.md) 屬性設定為提供的 patch 封裝路徑。<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | 叫用安裝，並針對 patch 套件所列出的每個產品，將 [**patch 屬性設定為修補程式**](patch.md) 套件的路徑，使其符合接收修補程式的資格。<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | 從 sourcelist 中移除所有網路來源。<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | 叫用收集和儲存使用者資訊和產品代碼的使用者介面 wizard 順序。<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | 設定產品功能的已安裝狀態。<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | 安裝或卸載產品。<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | 產生公告腳本。<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | 傳回具有所要求欄位數目的新 [**記錄**](record-object.md) 物件。<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | 針對目前進程空間中的所有後續安裝會話，啟用所選訊息類型的記錄。<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | 將修補程式的資訊以 XML 字串的形式解壓縮。<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | 取得檔案的路徑，並傳回該檔案的128位雜湊。<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | 取得檔案的路徑，並傳回代表雜湊或編碼憑證的位元組的 **SAFEARRAY** 。<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | 傳回指定檔案的大小。<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | 傳回指定路徑的版本字串或語言字串。<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | 在下次需要來源時，強制安裝程式在來源清單中搜尋有效的產品來源。<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | 開啟安裝程式套件，並初始化安裝會話。<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | 傳回 [**記錄**](record-object.md) 物件，其中包含產生錯誤記錄之函式的最新錯誤的錯誤參數。<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | 開啟現有的資料庫，或建立一個新的資料庫。<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | 開啟安裝程式套件，以搭配存取產品資料庫和安裝引擎的函式使用。<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | 使用產品代碼開啟已安裝產品的安裝程式套件。<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | 傳回元件的已安裝路徑。<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | 傳回完整的元件路徑，並執行任何必要的安裝。<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | 傳回完整的元件路徑，並執行任何必要的安裝。<br/>                                                                                                             |
| [**RegistryValue**](installer-registryvalue.md)                         | 讀取指定之登錄機碼值的相關資訊。<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | 重新安裝功能，或更正已安裝功能的問題。<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | 重新安裝產品，或更正已安裝產品中的安裝問題。<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | 移除一或多個有資格接收修補程式的產品修補程式。 <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | 遞增特定功能的使用計數，並傳回該功能的安裝狀態。<br/>                                                                             |



 

### <a name="properties"></a>屬性

**安裝程式** 物件具有這些屬性。



| 屬性                                                                    | 存取類型           | Description                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | 傳回 [**RecordList**](recordlist-object.md) 物件，這個物件會列出使用指定已安裝元件的產品。<br/> **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | 傳回 [**StringList**](stringlist-object.md) 物件，列舉指定元件的一組用戶端。<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | 傳回已安裝元件的完整路徑。<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | 傳回 [**RecordList**](recordlist-object.md) 物件，這個物件會提供指定已安裝元件的完整路徑。 <br/> **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | 傳回 [**StringList**](stringlist-object.md) 物件，列舉指定元件的已註冊限定詞集合。<br/>                                                                                                          |
| [**單元**](installer-components.md)<br/>                       |                       | 傳回 [**StringList**](stringlist-object.md) 物件，以列舉所有產品的已安裝元件集合。<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | 傳回 [**RecordList**](recordlist-object.md) 物件，這個物件會列出已安裝的元件。<br/> **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                                    |
| [**環境**](installer-environment.md)<br/>                     | 讀取/寫入<br/> | 目前進程之環境變數的字串值。<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | 指定功能的父項功能。<br/>                                                                                                                                                                                                  |
| [**功能**](installer-features.md)<br/>                           |                       | 傳回 [**StringList**](stringlist-object.md) 物件，以列舉指定產品的已發行功能集。<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | 傳回功能的已安裝狀態。<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | 傳回已使用功能的次數。<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | 傳回上次使用指定功能的日期。<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | 傳回數位，表示檔案或資料夾之指定路徑的合併檔案屬性。<br/>                                                                                                                                  |
| [**補丁**](installer-patches.md)<br/>                             |                       | 傳回 [**StringList**](stringlist-object.md) 物件，其中包含套用至產品的所有修補程式。<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | 列舉 [**Patch**](patch-object.md) 物件的集合。<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | 傳回 [**StringList**](stringlist-object.md) 物件，其中包含可由提供的修補程式清單更新的檔案清單。<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | 傳回修補程式的相關資訊。<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | 傳回以分號分隔的轉換清單，這些轉換位於指定的 patch 封裝中，並套用至指定的產品。<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | 如果產品是受管理的，則傳回 True，如果產品未受管理，則傳回 False。<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | 傳回已安裝或已發佈產品的指定屬性值。<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | 傳回儲存在公告腳本中的指定屬性值。<br/>                                                                                                                                                         |
| [**產品**](installer-products.md)<br/>                           |                       | 傳回 [**StringList**](stringlist-object.md) 物件，列舉針對目前使用者和電腦安裝或公告的所有產品集。 <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | 列舉 [**產品**](product-object.md) 物件的集合。<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | 傳回產品的安裝狀態資訊。<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | 傳回描述限定元件的文字字串。<br/>                                                                                                                                                                               |
| [**RelatedProducts**](installer-relatedproducts.md)<br/>             |                       | 傳回 [**StringList**](stringlist-object.md) 物件，此物件會列舉其屬性工作表中具有指定 [**UpgradeCode**](upgradecode.md) 屬性之目前使用者和電腦的所有已安裝或公告的產品集合。<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | 檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | 傳回 [**SummaryInfo**](summaryinfo-object.md) 物件，這個物件可以用來檢查、更新和加入屬性至封裝或轉換的摘要資訊資料流程中。<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | 讀取/寫入<br/> | 表示在目前的進程空間內開啟和處理後續封裝時，所要使用的使用者介面型別。<br/>                                                                                                           |
| [**版本**](installer-version.md)<br/>                             |                       | 傳回目前版本 Windows Installer 的字串表示。<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 Automation 介面](using-the-automation-interface.md)
</dt> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




