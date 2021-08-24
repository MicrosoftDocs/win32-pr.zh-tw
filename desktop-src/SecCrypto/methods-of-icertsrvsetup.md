---
description: 下列方法是由 ICertSrvSetup 介面所定義。 這裡不會顯示內容存取方法。 若要查看 ICertSrvSetup 的屬性，請參閱 ICertSrvSetup 的屬性。
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: ICertSrvSetup 的方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407888"
---
# <a name="methods-of-icertsrvsetup"></a>ICertSrvSetup 的方法

下列方法是由 [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) 介面所定義。 這裡不會顯示內容存取方法。 若要查看 **ICertSrvSetup** 的屬性，請參閱 [ICertSrvSetup 的屬性](properties-of-icertsrvsetup.md)。



| 方法                                                                         | 描述                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | 將憑證授權單位單位 (CA) 憑證及其相關聯的私密金鑰匯入至 "LocalMachine" 存放區。                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | 取得 CA 設定的屬性值。                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | 取得 **CCertSrvSetupKeyInformation** 物件的集合，這些物件代表目前安裝在電腦上的有效 CA 憑證。                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | 針對非對稱金鑰簽章演算法，取得指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 所支援的雜湊演算法清單。 |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | 取得指定之 CSP 所支援的金鑰長度清單。                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | 取得指定之 CSP 針對非對稱簽章金鑰演算法儲存的金鑰容器名稱清單。                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | 取得在電腦上提供非對稱金鑰簽名演算法的 Csp 清單。                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | 取得可在電腦上以呼叫端內容安裝的 Ca 類型。                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | 使用預設值初始化 **CCertSrvSetup** 物件，以啟用 CA 角色的安裝。                                                                                                                                                           |
| [**安裝**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | 安裝 **CCertSrvSetup** 物件中所設定的 CA 角色。                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | 向呼叫端表示是否可以編輯指定的屬性。                                                                                                                                                                                       |
| [**卸載後**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | 不會執行，並保留供日後使用。                                                                                                                                                                                                        |
| [**卸載前**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | 暫時儲存角色特定的狀態資訊。                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | 設定 CA 一般名稱和選擇性的辨別名稱尾碼。                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | 設定 CA 設定的屬性值。                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | 設定 CA 角色的資料庫相關資訊。                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | 設定次級 CA 設定的父 CA 資訊。                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | 設定 CA 網頁註冊角色的 CA 資訊。                                                                                                                                                                                                   |



 

 

 
