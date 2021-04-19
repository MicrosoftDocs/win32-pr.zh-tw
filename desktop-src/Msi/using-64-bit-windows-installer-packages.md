---
description: 撰寫64位 Windows Installer 套件時，請遵循下列指導方針。
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: 使用64位 Windows Installer 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b46ab8a9668d816ea99bd92c2575e9ea6367352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981011"
---
# <a name="using-64-bit-windows-installer-packages"></a>使用64位 Windows Installer 套件

當您建立 [64 位 Windows Installer 封裝](64-bit-windows-installer-packages.md) 或呼叫 Windows Installer 以安裝64位封裝的應用程式時，請執行下列動作：

-   使用200或更高版本的 Windows Installer 資料庫架構。 將 [ [**頁面計數摘要**](page-count-summary.md) ] 屬性設定為整數200，以指定版本2.0 是安裝封裝所需的最小安裝程式版本。 舊版 Windows Installer 拒絕安裝64位套件的嘗試。 若為 Arm64 平臺上的64位封裝，Windows Installer 資料庫架構必須是500或更新版本。
-   在封裝摘要資訊資料流程的 [ [**範本摘要**](template-summary.md) ] 屬性中，指出這是64位封裝。 如果封裝要在 Intel64 處理器上執行，請在 [ **範本摘要** ] 屬性的 [平臺] 欄位中輸入 "Intel64"。 如果封裝要在64位的擴充處理器上執行，請輸入 "x64"。 如果封裝要在 Arm64 處理器上執行，請輸入 "Arm64"。 無法將套件標示為支援 Intel64 和 x64 平臺， **範本摘要** 屬性值 "Intel64，x64" 無效。 封裝不能標示為支援32位和64位平臺，「Intel，x64」或「Intel，Intel64」的 **範本摘要** 屬性值無效。
-   在 [元件](component-table.md)資料表的 [屬性] 資料行中設定 **msidbComponentAttributes64bit** ，以識別每個64位元件。
-   使用選擇性的條件陳述式，藉由參考 [**VersionNT64**](versionnt64.md) 屬性來檢查64位作業系統的版本。 Windows Installer 將此屬性設定為64位 Windows 版本，並在作業系統不是64位 Windows 時將 VersionNT64 保留為未定義。 如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。
-   使用選擇性的條件陳述式，藉由參考 [**Intel64**](intel64.md) 或 [**Msix64**](msix64.md) 屬性來檢查電腦的數值處理器等級。 Windows Installer 將這些屬性設定為電腦目前的數值處理器層級，並在這不是 Itanium 型處理器時，將 **Intel64** 屬性保留為未定義。 如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。
-   使用 [AppSearch 資料表](appsearch-table.md) 和 [AppSearch 動作](appsearch-action.md) 來針對現有的64位元件執行登錄的選擇性搜尋。 若要搜尋現有的64位元件，請在 [RegLocator 資料表](reglocator-table.md)的 Type 資料行中包含 **msidbLocatorType64bit** 位。 如需詳細資訊，請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案屬性](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   藉由參考64位資料夾的 [**System64Folder**](system64folder.md)屬性、 [**ProgramFiles64Folder**](programfiles64folder.md) 屬性和 [**CommonFiles64Folder**](commonfiles64folder.md) 屬性，以及32位資料夾的 [**SystemFolder**](systemfolder.md) 屬性、 [**ProgramFilesFolder**](programfilesfolder.md) 屬性和 [**CommonFilesFolder**](commonfilesfolder.md) 屬性，來取得系統資料夾的路徑。
-   參考64位元件時，請確認應用程式使用正確的 GUID。 如果有32位和64位版本的特定元件，則這些元件必須有不同的元件識別碼 Guid。
-   判斷在安裝64位應用程式時是否需要定義任何新的環境變數。
-   如果要安裝64位 ODBC 驅動程式管理員，則攜帶該驅動程式的元件應該命名為 ODBCDriverManager64。 ODBC 驅動程式管理員必須在安裝程式套件中撰寫，且必須包含名為 ODBCDriverManager64 的元件。 如有必要，將會安裝管理員。
-   確認應用程式只會呼叫以可執行檔形式執行的32位服務。 應用程式不應呼叫在 Dll 中執行的32位服務。
-   如果應用程式安裝並存的32位和64位版本的元件，請確認應用程式已正確共用 .ini 檔案資訊。
-   確認應用程式只會將32位修補程式套用至32位二進位檔，並將64位修補程式套用至64位二進位檔。
-   針對32位和64位版本，請考慮未來的升級案例，並維護升級程式碼。 如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。
-   使用啟動載入 [應用程式](bootstrapping.md) 安裝 [64 位 Windows Installer 套件](64-bit-windows-installer-packages.md)時，請將啟動載入應用程式編譯為64位應用程式。
-   若要針對受特定元件影響的登錄機碼停用登錄 [反映](../winprog64/registry-reflection.md)，請在 [元件](component-table.md)資料表的 [屬性] 欄位中設定 **msidbComponentAttributesDisableRegistryReflection** 位。 這可能需要將相同應用程式的32位和64位複本並存。 如果設定此位，Windows Installer 會在元件所存取的每個索引鍵上呼叫 [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) 函數。 這位 Windows Installer 版本4.0 提供。 32位系統會忽略此位。 64位版本的 Windows XP 和 Windows 2000 會忽略此位。

> [!Note]  
> [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)函數的 *lpPathBuf* 參數所傳回的數值登錄根目錄值，會區分32位和64位作業系統上的元件。 如需詳細資訊，請參閱 **MsiGetComponentPath** 函數。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[64位自訂動作](64-bit-custom-actions.md)
</dt> </dl>

 

 
