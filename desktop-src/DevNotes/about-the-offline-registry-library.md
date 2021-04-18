---
description: 離線登錄庫是用來修改作用中系統登錄外部的登錄 hive。
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: 關於離線登錄庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468013"
---
# <a name="about-the-offline-registry-library"></a>關於離線登錄庫

離線登錄庫是用來修改作用中系統登錄外部的登錄 hive。

離線登錄庫適用于登錄更新案例，例如服務作業系統映射。 離線登錄函式提供標準登錄功能無法使用的下列功能：

-   離線登錄功能可以用來修改任何支援的登錄格式的登錄 hive。 標準登錄函式只能變更作用中的登錄區，而變更必須與系統上執行的 Windows 版本相容。
-   離線登錄庫只需要讀取權限，即可開啟登錄 hive 檔案和寫入存取權來儲存檔案。 系統不會對 hive 中的物件執行其他存取檢查，因此可以使用標準使用者權限來修改 hive。 使用標準登錄功能時，將 hive 載入 active registry 是需要系統管理存取權的特殊許可權作業。

離線登錄功能不應該用來代替系統登錄功能，原因如下：

-   使用離線登錄功能時，無法在進程之間共用登錄 hive。
-   離線登錄函式使用簡單的鎖定，可能會對多執行緒應用程式造成嚴重的效能降低。
-   在呼叫 [**ORSaveHive**](orsavehive.md) 函式之前，不會儲存離線登錄功能所做的變更。

應用程式不應該使用離線登錄功能來略過系統登錄的安全性需求。 若要載入 hive，在沒有 [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式所需特殊許可權的情況下執行的應用程式可以使用 [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) 函數。

**Windows Server 2003 和 WINDOWS XP：** 不支援 [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) 函數。

*離線登錄 hive* 是已使用離線登錄功能載入至記憶體的登錄 hive。 若要建立空白的離線登錄 hive，請使用 [**ORCreateHive**](orcreatehive.md) 函數。 若要修改現有的登錄區，請使用 [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) 或 [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) 函式，將 hive 從 active system 登錄儲存至檔案，然後使用 [**OROpenHive**](oropenhive.md) 函數來開啟檔案。

[**ORCreateHive**](orcreatehive.md)和 [**OROpenHive**](oropenhive.md)函式會將控制碼傳回給離線登錄區的根機碼。 這個控制碼可作為離線登錄區中任何其他金鑰的控制碼，但有下列例外狀況： [**ORCreateKey**](orcreatekey.md) 和 [**OROpenKey**](oropenkey.md) 函式不能用來傳回根金鑰的控制碼; [**ORCloseKey**](orclosekey.md) 函式不能用來關閉根金鑰;而且 [**ORDeleteKey**](ordeletekey.md) 函式無法用來刪除根金鑰。 在上述所有情況下，此函式會失敗，並出現 **錯誤 \_ \_ 參數無效**。

您可以使用 [**ORCreateKey**](orcreatekey.md) 函式，將金鑰新增至開啟的離線登錄 hive，並使用 [**ORSetValue**](orsetvalue.md) 函式來設定索引鍵的值。 離線登錄庫支援其他基本登錄作業，例如列舉、取出和刪除機碼和值，以及設定索引鍵屬性，例如安全性和虛擬化行為。 如需函式的清單，請參閱離線登錄連結 [庫函數](offline-registry-library-functions.md)。

若要儲存對開啟離線登錄區的變更，請使用 [**ORSaveHive**](orsavehive.md) 函式將 hive 儲存至檔案。  (除非呼叫 **ORSaveHive** ，否則不會保存變更。 ) 儲存 hive 之後，請使用 [**ORCloseHive**](orclosehive.md) 函式來關閉 hive 和與其相關聯的可用資源。

只有在使用 [**OROpenHive**](oropenhive.md) 函式開啟離線登錄 hive 時，才會進行驗證。 如果 hive 損毀，作業就會失敗;不嘗試修復 hive。 在使用 [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式將 hive 載入至作用中登錄之前，不會執行 hive 中物件的存取檢查。

離線登錄功能不支援 [預先定義的金鑰](../sysinfo/predefined-keys.md)。

傳遞至離線登錄函式的所有索引鍵和值名稱字串都必須是 Unicode。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[離線登錄庫 \_ 函數](offline-registry-library-functions.md)
</dt> </dl>

 

 
