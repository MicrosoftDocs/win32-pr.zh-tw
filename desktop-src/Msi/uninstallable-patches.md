---
description: 是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: 可卸載修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a3abea369a09dd51e995ba28dcab1463032bb6e5dec9648d3eae39be4cbf21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527638"
---
# <a name="uninstallable-patches"></a>可卸載修補程式

是否可以卸載修補程式取決於修補程式的撰寫方式、用來安裝修補程式的 Windows Installer 版本，以及修補程式對應用程式所做的變更。 如果未可卸載修補程式，則移除修補程式的唯一方法是卸載整個應用程式，並重新安裝，而不套用即將移除的修補程式。

您可以使用 [命令列選項](command-line-options.md)、 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函式或 [**RemovePatches 方法**](installer-removepatches.md)（如 [卸載修補程式](uninstalling-patches.md)一節中所述），呼叫卸載隨 Windows Installer 3.0 版套用的修補程式。 Windows Installer 會確認在 [**MSIPATCHREMOVE**](msipatchremove.md)屬性中所列出的每個修補程式都已可卸載。 如果使用者沒有移除修補程式的許可權、修補程式對產品而言是未知的、修補原則會防止移除，或修補程式標示為非可卸載，則安裝程式會傳回指出失敗的安裝交易的錯誤。

**Windows Installer 2.0：** 不支援。 使用早于 Windows Installer 3.0 的 Windows Installer 版本所套用的修補程式則不會可卸載。

## <a name="patches-that-are-not-uninstallable"></a>未可卸載的修補程式

在下列情況下，不會可卸載套用至已安裝應用程式) 的 patch ( .msp 檔案。 移除未可卸載之修補程式的唯一方法是卸載已修補的應用程式，然後重新安裝應用程式，而不需要重新套用修補程式。 在此情況下，您必須重新套用任何您不想要從應用程式移除的修補程式。

-   使用 Windows Installer 小於 Windows Installer 3.0 的版本所套用的修補程式則不會可卸載。
-   套用至安裝在系統管理員所設定之 [DisablePatchUninstall](disablepatchuninstall.md) 原則之電腦上的應用程式的修補程式，並不會可卸載。 當設定此 [電腦原則](machine-policies.md)時，即使是系統管理員，也不能卸載電腦上的任何修補程式。
-   在資料庫中沒有 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表的修補程式不會可卸載。
-   未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含下列資料列的修補程式則不會可卸載。 不會可卸載公司、屬性和值的其他值的修補程式。

    | 公司 | 屬性     | 值 |
    |---------|--------------|-------|
    | ;  | AllowRemoval | 1     |

    

     

-   修補程式已套用至安裝在內容中的應用程式，但使用者沒有足夠的許可權可卸載修補程式。 下表中的「不允許」單字表示系統管理員或非系統管理員的使用者無法從已在此內容中安裝的已修補應用程式卸載修補程式。 此表格中的「允許」一字表示許可權並不會防止系統管理員或非系統管理員使用者卸載修補程式，但基於本節所討論的任何其他原因，仍然可能無法卸載修補程式。

    | 應用程式安裝內容        | 系統管理員卸載修補程式 | 非系統管理員卸載修補程式                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | 允許                          | 通常不允許唯一的例外狀況是使用 (LUA) 修補來套用修補程式。 系統管理員或非系統管理員會可卸載標示為 LUA 修補程式的修補程式。 LUA 修補僅適用于每台電腦從媒體安裝的套件，且需要特殊的撰寫。<br/> |
    | 針對目前使用者 Per-User 非受控   | 允許                          | 允許                                                                                                                                                                                                                                                                                                          |
    | 針對不同的使用者 Per-User 非受控 | 不允許                      | 不允許                                                                                                                                                                                                                                                                                                      |
    | 目前使用者的 Per-User 管理       | 允許                          | 不允許                                                                                                                                                                                                                                                                                                      |
    | 針對不同使用者管理 Per-User     | 不允許                      | 不允許                                                                                                                                                                                                                                                                                                      |

    

     

-   未可卸載修補程式所套用的 [主要升級](major-upgrades.md) 。 應用程式的主要升級應藉由將升級的應用程式安裝 (.msi 檔) 而不是修補程式來執行。
-   未可卸載套用至系統管理安裝的修補程式。 不建議您修補系統管理安裝。 使用者從系統管理映射安裝應用程式之後，應該在使用者的電腦上套用一組目前的修補程式。 這可防止使用者電腦上快取的 [套件程式碼](package-codes.md) 與系統管理安裝上的套件程式碼不同。 如果使用者電腦上快取的套件程式碼與系統管理安裝上的不同，請從系統管理安裝重新安裝該應用程式，然後再修補用戶端電腦。
-   當 patch 將新內容新增至下列清單中的任何資料表時，Windows Installer 將修補程式標示為未可卸載。 可卸載修補程式可以將新的資料列新增至不包含在此清單中的資料庫資料表，以將新的檔案、元件、登錄專案、元件或功能加入至安裝中。

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [類別](class-table.md)
    -   [Complus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [環境](environment-table.md)
    -   [延伸模組](extension-table.md)
    -   [Font](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [MIME](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [ProgId](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [類型](typelib-table.md)
    -   [動詞命令](verb-table.md)
    -   [!Note]  
        > 如果 patch 將新內容加入至[RemoveFile](removefile-table.md)或[RemoveRegistry](removeregistry-table.md)資料表，Windows Installer 不會將修補程式標示為未可卸載。 不過，除非原始安裝套件中尚未存在用來移除新內容的資源，否則不會可卸載修補程式。 例如，如果 patch 將新的資料列新增至 RemoveFile 資料表，則如果檔案位於檔案 [資料表](file-table.md)外部，則無法藉由卸載修補程式來還原移除的檔案。 檔案必須已在原始封裝的檔案資料表中撰寫，並套用修補程式以可卸載修補程式。

         

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補程式順序](sequencing-patches.md)
</dt> <dt>

[移除修補程式](removing-patches.md)
</dt> <dt>

[卸載修補程式](uninstalling-patches.md)
</dt> <dt>

[修補卸載自訂動作](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




