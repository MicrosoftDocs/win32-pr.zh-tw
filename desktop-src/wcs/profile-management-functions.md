---
title: 設定檔管理功能
description: 設定檔管理功能
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- WCS 參考，設定檔
- WCS 的參考，設定檔
- 設定檔管理
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106993767"
---
# <a name="profile-management-functions"></a>設定檔管理功能

## <a name="profile-management-functions"></a>設定檔管理功能

下列 API 函數在設定檔管理中很有用。



| 函式                                                                               | 描述                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | 將指定的色彩設定檔與指定的裝置產生關聯。                                                              |
| [**CreateProfileFromLogColorSpaceW**] ( (/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)  | 將邏輯 [色彩空間](c.md) 轉換成 [裝置設定檔](d.md)。 |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | 解除指定的色彩設定檔與指定電腦上的指定裝置。 |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | 列舉滿足指定列舉準則的所有設定檔。 |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | 抓取指定電腦上 Windows COLOR 目錄的路徑。 |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | 從直接色彩顯示面板取得 gamma 曲線。                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | 抓取已針對指定標準 [色彩空間](c.md)註冊的色彩設定檔。 |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | 安裝指定的設定檔，以便在指定的電腦上使用。 設定檔也會複製到 COLOR 目錄。 |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | 將指定的識別值與指定的色彩管理模組動態連結程式庫產生關聯 (的 CMM DLL) 。 當此識別碼出現在色彩設定檔中時，Windows 可以找到對應的 CMM，以便建立轉換。 |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | 設定直接色彩顯示面板上的 gamma 曲線。                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | 針對指定的標準 [色彩空間](c.md)，註冊指定的設定檔。 您可以使用 [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)來查詢設定檔。 |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | 從指定的電腦移除指定的色彩設定檔。 相關聯的檔案會選擇性地從系統中刪除。 |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | 從指定的色彩管理模組動態連結程式庫分離指定的識別碼值， (CMM DLL) 。 |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | 將指定的 WCS 色彩設定檔與指定的裝置產生關聯。                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | 將 WCS 設定檔轉換成 ICC 設定檔。                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | 解除指定的 WCS 色彩設定檔與指定電腦上的指定裝置。                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | 列舉符合指定設定檔管理範圍中的列舉準則的所有色彩設定檔。                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | 傳回 [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) 函式列舉色彩設定檔所需的緩衝區大小（以位元組為單位）。 |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | 抓取裝置的預設色彩設定檔，或如果未指定裝置，則抓取與裝置無關的預設設定檔。                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | 傳回裝置預設色彩設定檔名稱的大小（以位元組為單位），包括 **Null** 結束字元。                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | 抓取指定設定檔管理範圍中的預設轉譯意圖。                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | 判斷使用者是否已選擇針對指定的裝置使用每個使用者設定檔關聯清單。                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | 建立指定之色彩設定檔的控制碼。                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | 設定指定設定檔管理範圍中指定配置檔案類型的預設色彩設定檔名稱。                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | 設定指定設定檔管理範圍中的預設轉譯意圖。                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | 允許使用者指定是否要針對指定的裝置使用每個使用者設定檔關聯清單。                                              |



 

## <a name="profile-consumption-functions"></a>設定檔耗用量函數

設定檔耗用量 Api 是 ICM2 中採用 ICC 或 WCS XML 設定檔、設定檔控制碼或轉譯意圖作為參數的 Api，以及一組適用于 WCS 設定檔的新 Api，可支援應用程式色彩管理程式碼。

 

## <a name="profiles-and-profile-management-functions"></a>設定檔和設定檔管理功能

設定檔管理工作流程是以現有的 ICM2 Api 為基礎，這些 Api 已增強，可提供額外的功能來修訂應用程式程式碼。

設定檔包含色彩處理演算法用來轉譯不同色彩空間之間色彩的資訊。 設定檔管理提供一種方式來查詢和指定在不同階段使用哪些設定檔來處理色彩處理模型，以管理各種具有不同色彩特性的周邊裝置色彩輸出。

設定檔管理提供下列一組功能：

 

1. 安裝色彩設定檔以供系統使用。

 

2. 將一或多個已安裝的色彩設定檔與任何特定裝置產生關聯。

 

3. 在設定檔中選擇特定類型的預設色彩設定檔，可用於特定的色彩處理階段。 這可能適用于裝置相關設定檔中的裝置，或安裝在系統中的設定檔，而不是特定裝置。

 

4. 列舉色彩設定檔，以滿足系統中所安裝設定檔之間的特定準則。

WCS 設定檔的副檔名為 ". cdmp" （適用于 DMPs）、". camp" （Camp）和 ". gmmp" （適用于 GMMPs）。

 

**每個使用者設定檔管理，並在 LUA 內容中啟用執行**

目前檔中所述的設計目標如下所示：

 

1. 舊版 ICM2 的執行不提供個別使用者設定檔管理的支援。 不同的使用者不能有自己的設定檔設定。 在 Vista 中，WCS 設定檔管理基礎結構可讓使用者針對大部分功能設定個別的設定檔設定。

 

2. 所有舊版 ICM2 設定檔管理 Api 都會修改整個系統的設定，而且需要系統管理許可權。 在 Windows Vista 中，所有使用者都是在最低許可權的使用者帳戶中執行， (LUA) 設定，而系統管理員可以選擇性地提升許可權，以執行修改全系統設定的應用程式。 在 WCS 設定檔管理中，所有每個使用者的設定檔設定都可在 LUA 內容中進行設定。 設定檔管理應用程式可以執行為 LUA 設定，增加其使用範圍，並確保系統的安全性不會受到危害。

Vista 中的設定檔管理提供下列優於舊版 ICM2 基礎結構的增強功能：

 

1. 它可讓設定檔與裝置、預設設定檔設定，以及列舉每個使用者和整個系統範圍中的設定檔相關聯。

 

2. 安裝設定檔會維持系統的範圍，而且需要系統管理員許可權。 這與裝置安裝期間的設定檔安裝一致，因為裝置安裝全系統，且需要系統管理許可權。

 

是否可以從 LUA 內容安裝裝置，是針對該類別的裝置所支援的裝置。 例如，在 Vista 中，如果使用者已被授與使用驅動程式存放區原則的網域系統管理員將檔案複製到驅動程式存放區的許可權，就可以從 LUA 內容進行印表機安裝。 色彩設定檔管理基礎結構不需要在這方面做任何特殊的動作，因為安裝會在多工緩衝處理器內容中進行。

 

3. 修改每個使用者範圍中的設定檔設定可以在 LUA 內容中完成;需要系統管理許可權的全系統修改。 需要讀取設定資訊的設定檔管理作業，可以在每個使用者和全系統設定的 LUA 內容中完成。

設定檔管理範圍表示執行的作業範圍;每位使用者或整個系統。

針對每個作業，其會指出是否可以從 LUA 內容進行。 如果無法在 LUA 內容中執行作業，對應的設定檔管理 API 會傳回失敗並拒絕存取。 使用 API 的應用程式（例如色彩管理主控台）可以讓使用者使用 OTS 或同意 UI) 提升至系統管理內容 (，然後從提高許可權的內容中呼叫 API，如此作業才會成功。



作業

設定檔管理範圍

前置條件

後置條件

LUA 內容中的可執行檔

$ {ROWSPAN2} $Install 設定檔 $ {REMOVE} $  

全系統

設定檔已複製、安裝到系統中，並且可供使用。 所有使用者的整個系統和目前使用者範圍中的設定檔是可列舉的。

在安裝設備磁碟機時，受驅動程式安裝原則所規範。 否，否則為。

目前使用者

不支援

$ {ROWSPAN2} $Uninstall 設定檔 $ {REMOVE} $  

全系統

設定檔安裝在系統中

從系統卸載的設定檔，並選擇性地從設定檔存放區刪除。 設定檔無法再使用，且在任何範圍中都不可列舉。

No

目前使用者

不支援

具有裝置 $ {REMOVE} $ 的 $ {ROWSPAN2} $Associate 設定檔  

全系統

設定檔已安裝，且其類型為 ICC 或 CDMP

所有使用者都可以使用設定檔來與裝置搭配使用。 它是可列舉的，適用于全系統範圍，以及與裝置相關聯之所有使用者的目前使用者範圍。

No

目前使用者

已安裝設定檔。 設定檔是否已經與全系統範圍中的裝置相關聯，而且屬於 ICC 或 CDMP 類型，並不重要。

目前的使用者可以使用設定檔來與裝置搭配使用。 它只有在目前使用者的範圍內是可列舉的 (除非有與裝置相關聯的全系統關聯) 。

Yes

來自裝置 $ {REMOVE} $ 的 $ {ROWSPAN2} $Disassociate 設定檔  

全系統

設定檔與整個系統範圍中的裝置相關聯，且類型為 ICC 或 CDMP

設定檔已不再可供使用 (除了其目前使用者範圍內具有此關聯的使用者，也) 。 它在整個系統範圍中不可列舉。 但是，對於在其範圍內具有這個關聯的使用者而言，它可以在目前使用者的範圍內列舉。

No

目前使用者

設定檔與目前使用者範圍中的裝置相關聯 (無論它是否與整個系統範圍) 相關聯，且其類型為 ICC 或 CDMP。

設定檔已無法再使用，或與裝置相關聯的可列舉（依目前使用者 (），除非它也與裝置) 的全系統範圍相關聯。

Yes

$ {ROWSPAN2} $Set 配置檔案類型 (DMP 或 ICC) 作為裝置 $ {REMOVE} $ 的預設值  

全系統

設定檔的類型為 ICC 或 CDMP

此設定檔預設會用於裝置的特定類型，除了在其目前使用者範圍中覆寫此設定的使用者之外。  (設定檔已安裝並與裝置系統寬度相關聯（如果尚未安裝的話）。 ) 

No

目前使用者

設定檔的類型為 ICC 或 CDMP

預設會在目前使用者的情況下，針對特定類型與裝置使用設定檔，而不考慮這個的全系統預設。  (設定檔已安裝，並與目前使用者的裝置產生關聯（如果沒有的話）。 ) 

是，如果已安裝設定檔

$ {ROWSPAN2} $Set 設定檔的類型 (ICC、DMP、CAMP、GMMP) 和子類型組合，作為全域預設 $ {REMOVE} $  

全系統

只有 ICC 和 CDMP 設定檔可以與裝置建立關聯。

預設會針對特定類型使用設定檔。 使用者可以在目前使用者的範圍內覆寫此設定。  (已安裝設定檔（如果尚未安裝的話）。 ) 

No

目前使用者

只有 ICC 和 CDMP 設定檔可以與裝置建立關聯。

預設會針對目前使用者的特定類型使用設定檔。  (已安裝設定檔（如果尚未安裝的話）。 ) 

是，如果已安裝設定檔。

$ {ROWSPAN2} $Erase 特定預設設定檔設定的目前使用者覆寫，如此一來，系統預設一律會使用 (作為 fallback) 即使是目前使用者的範圍。 $ {REMOVE} $  

全系統

不適用

目前使用者

即使是針對預設設定檔設定的最新使用者查詢，也會傳回整個系統的設定，以供使用。

Yes

$ {ROWSPAN2} $Enumerate 已安裝的設定檔，滿足特定準則 (例如裝置類別、設定檔類別等等。 ) $ {REMOVE} $  

全系統

只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。

系統會列舉已安裝且符合全系統範圍中指定之準則的設定檔。

Yes

目前使用者

只有 ICC 和 CDMP 設定檔可以與裝置建立關聯，因此會針對裝置進行列舉。

系統會列舉已安裝且符合全系統範圍中指定之準則的設定檔。

Yes

$ {ROWSPAN2} $Enumerate 設定檔與滿足特定條件的特定裝置相關聯，例如裝置類別和設定檔類別 $ {REMOVE} $  

全系統

只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。

系統會列舉與整個系統範圍中的裝置相關聯的設定檔，並符合全系統範圍中指定的準則。

Yes

目前使用者

只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。

與目前使用者範圍中的裝置相關聯的設定檔（包括系統範圍的關聯）以及滿足目前使用者範圍中指定的準則，都會加以列舉。

Yes



 

有效的色彩配置檔案類型是由 COLORPROFILETYPE 列舉所提供。

有效的色彩設定檔子類型是由 COLORPROFILESUBTYPE 列舉所提供。

下表顯示有效的配置檔案類型/子類型組合。



COLORPROFILETYPE

有效的 COLORPROFILESUBTYPE

備註

裝置預設

全域預設值

預定用途

預定用途

CPT \_ ICC

CPST \_ 無

取得/設定與裝置相關聯的預設 ICC 設定檔

CPST \_ RGBWorkingSpace 或 CPST \_ CustomWorkingSpace

取得/設定 ICC 設定檔為全域 RGB 或自訂工作空間設定檔。 請參閱附註。

COLORPROFILETYPE CPT \_ ICC 和 CPT \_ DMP 互相排斥。 您為指定工作空間設定的預設色彩設定檔 (RGB 或自訂) 可以是 ICC 設定檔或 DMP 設定檔，但不能同時為兩者。

CPT \_ DMP

CPST \_ 無

取得/設定與裝置相關聯的預設 DMP 設定檔

CPST \_ RGBWorkingSpace 或 CPST \_ CustomWorkingSpace

取得/設定 DMP 設定檔為全域 RGB 或自訂工作空間設定檔。 請參閱附註。

COLORPROFILETYPE CPT \_ ICC 和 CPT \_ DMP 互相排斥。 您為指定工作空間設定的預設色彩設定檔 (RGB 或自訂) 可以是 ICC 設定檔或 DMP 設定檔，但不能同時為兩者。



 

> [!Note]  
> 呼叫 WcsSetDefaultColorProfile 以將 DMP 設定檔設定為 RGB 工作空間或自訂工作空間的預設設定檔時，只有類型為 RGBVirtualDevice、LCD 或 CRT 的 DMP 設定檔是有效的。
>
>  
>
> 當呼叫 WcsSetDefaultColorProfile 來將 ICC 設定檔設定為 RGB 工作空間或自訂工作空間的預設設定檔時，只有其類別為 "spac" 或 "" 且色彩空間為 "RGB" 的 ICC 設定檔才有效。

 

此架構是根據上述列舉和資料表中所述的作業需求所設計。

### <a name="profile-management-public-api-layer"></a>設定檔管理公用 API 層

由於舊版 ICM2 Api 不支援設定檔管理範圍，因此需要一組新的 WCS 設定檔管理 Api，將設定檔管理範圍定義為全系統或目前的使用者。 ? 舊版 ICM2 Api 會繼續支援以提供回溯相容性，並使用對呼叫隱含的設定檔管理範圍。 o ICM2 可在目前使用者範圍上運作的 Api？ 這是針對在 WCS 設定檔管理中，系統範圍和目前使用者範圍所支援的作業。 舊版 ICM2 Api 會以目前使用者的設定檔管理範圍，在新的 WCS Api 上呼叫。 從使用者的角度來看，這是合理的，因為這可讓您從繼承應用程式進行個別使用者的設定，也可以在 LUA 內容中執行大部分的作業。 o ICM2 可在整個系統範圍內運作的 Api？ 這適用于作業 (安裝設定檔和卸載設定檔，) 僅支援全系統範圍。 不會建立新的 WCS 設定檔管理 Api，而且可以修改現有的 Api。

設定檔管理作業的基礎會在下列設定資料實體上運作，以建立色彩處理演算法的內容以提供色彩管理功能。 它們是裝置特定或全域 (裝置獨立) 設定。 o 裝置特定設定資料：？ 與特定裝置相關聯的配置檔案清單。 ? 與裝置相關聯之不同配置檔案類型的預設設定檔。 ? 用於列舉的設定檔的比對模式。 o Global configuration data：？ 系統中安裝的配置檔案清單。 ? 不同配置檔案類型的全域預設設定檔。 ? 設定資料儲存體的基礎執行會在設定資料的儲存體範圍內進行， (裝置獨立或裝置特定的) （可以是全系統或目前的使用者）。 這與設定檔管理範圍不同。 如果該作業目前的使用者設定不存在，則具有目前使用者設定檔管理範圍的作業可能會從整個系統的儲存範圍中讀取。 ? ICM2/WCS API 層會在此儲存層中呼叫，以使用適當的儲存體範圍來取得和設定資料。 儲存層對設定檔管理範圍是透明的。 結合目前使用者和全系統儲存範圍的資料，根據 API 呼叫端所指定的設定檔管理範圍來建立或更新設定的邏輯。 此邏輯存在於 ICM2/WCS API 層中。

### <a name="device-specific-storage-layer"></a>裝置特定的儲存層

不同裝置類別的儲存體（例如列印、捕捉或顯示）可能會彼此不同。 例如，您必須使用標準列印 Api （例如 SetPrinterDataEx 和 GetPrinterDataEx）來儲存列印裝置的設定資料，讓設定檔得以複製，並在點對列印連線期間將設定傳送至用戶端電腦。 ? 這一層會使用一般預先定義的介面來匯出開啟存放區、取得資料、設定資料和關閉存放區的功能，讓設定檔管理設定儲存層可以在這些介面中呼叫這些介面，同時對該裝置的資料儲存方式是透明的。

下圖說明這個架構。



設定檔管理公用 API 層

$ {ROWSPAN2} $Legacy ICM2 Api 來進行僅支援 Vista 中全系統設定檔管理範圍的作業 (安裝、卸載，以及取得色彩目錄) 。 他們會以適當的儲存體範圍呼叫設定儲存層。 $ {REMOVE} $  

在 Vista 中支援全系統和目前使用者設定檔管理範圍之作業的舊版 ICM2 API (安裝、卸載和取得色彩目錄) 以外的所有作業。 它們會在目前使用者的範圍上隱含地運作，並以目前使用者的設定檔管理範圍呼叫新的 WCS API。

新的 WCS API，具備全系統和目前的使用者設定檔管理範圍支援。 他們會以適當的儲存體範圍呼叫設定儲存層。



 



設定檔管理設定儲存層

與裝置無關的全域設定常式

裝置特定設定常式

$ {ROWSPAN3} $Profile 安裝和與裝置無關的預設設定檔設定管理，其支援全系統和目前的使用者儲存範圍。 $ {REMOVE} $  

裝置關聯和裝置特定的預設設定檔設定管理，在全系統和目前使用者的儲存體範圍中受到支援。

Device-Specific 儲存層

列印特定的儲存體

顯示特定的儲存體

捕獲特定儲存體



 

在 Vista 中僅支援全系統設定檔管理範圍之作業的舊版 ICM2 Api 沒有任何行為變更。 安裝和卸載作業落在此類別中。

適用于支援全系統和目前使用者設定檔管理範圍之作業的舊版 ICM2 Api，其行為會變更為 [查詢] 和 [設定目前使用者] 設定。 安裝和卸載以外的所有作業都屬於此類別。

 

 




