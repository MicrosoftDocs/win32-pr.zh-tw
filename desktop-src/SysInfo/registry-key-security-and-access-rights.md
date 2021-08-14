---
description: Windows 的安全性模型可讓您控制對登錄機碼的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 266d5c8e-1bcd-48e5-bc06-2fbc956d8658
title: 登錄機碼安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0797eeff4923574007c2e1d7751121767c894f91a42316ff5d581ee2d18b6d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885201"
---
# <a name="registry-key-security-and-access-rights"></a>登錄機碼安全性與存取權限

Windows 的安全性模型可讓您控制對登錄機碼的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

當您呼叫 [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)或 [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)函式時，可以指定登錄機碼的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。 如果您指定 **Null**，索引鍵會取得預設安全描述項。 金鑰之預設安全描述項中的 Acl 會從其直接父機碼繼承。

若要取得登錄機碼的安全描述項，請呼叫 [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)、 [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa)或 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。

登錄機碼的有效存取權限包括刪除、讀取 \_ 控制、寫入 \_ DAC，以及寫入 \_ 擁有者 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。 登錄機碼不支援 [同步處理標準] 存取權限。

下表列出登錄機碼物件的特定存取權限。



| 值                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 重要的 \_ 所有 \_ 存取 (0xF003F) <br/>         | 結合必要的標準 \_ 許可權 \_ 、金鑰 \_ 查詢 \_ 值、金鑰 \_ 集 \_ 值、金鑰 \_ 建立 \_ 子機 \_ 碼、金鑰列舉子機碼 \_ \_ \_ 、金鑰 \_ 通知，以及金鑰 \_ 建立 \_ 連結存取權限。<br/>                                                                                                                                                                                                                                                                           |
| 金鑰 \_ 建立 \_ 連結 (0x0020) <br/>         | 保留供系統使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 金鑰 \_ 建立 \_ 子機碼 \_ (0x0004) <br/>     | 建立登錄機碼的子機碼所需。<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ \_ (0X0008) 的按鍵列舉子機碼<br/> | 列舉登錄機碼的子機碼所需。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| 金鑰 \_ 執行 (0x20019) <br/>             | 相當於 \_ 讀取的索引鍵。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 金鑰 \_ 通知 (0x0010) <br/>               | 要求登錄機碼或登錄機碼的子機碼變更通知所需。<br/>                                                                                                                                                                                                                                                                                                                                                              |
| \_ (0x0001) 的索引鍵查詢 \_ 值<br/>         | 查詢登錄機碼值的必要項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| 金鑰 \_ 讀取 (0x20019) <br/>                | 結合標準 \_ 許可權 \_ 讀取、金鑰 \_ 查詢 \_ 值、金鑰列舉子機碼 \_ \_ \_ 和金鑰 \_ 通知值。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| \_ (0x0002) 的索引鍵集 \_ 值<br/>           | 建立、刪除或設定登錄值所需。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| KEY \_ WOW64 \_ 32KEY (0x0200) <br/>         | 指出64位 Windows 上的應用程式應該在32位登錄視圖上運作。 32位 Windows 會忽略此旗標。 如需詳細資訊，請參閱 [存取替代登錄視圖](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)。<br/> 此旗標必須與下表中其他旗標（查詢或存取登錄值）結合使用 OR 運算子。<br/> **Windows 2000：** 不支援此旗標。<br/> |
| KEY \_ WOW64 \_ 64KEY (0x0100) <br/>         | 指出64位 Windows 上的應用程式應該在64位登錄視圖上運作。 32位 Windows 會忽略此旗標。 如需詳細資訊，請參閱 [存取替代登錄視圖](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)。<br/> 此旗標必須與下表中其他旗標（查詢或存取登錄值）結合使用 OR 運算子。<br/> **Windows 2000：** 不支援此旗標。<br/> |
| 金鑰 \_ 寫入 (0x20006) <br/>               | 結合標準的 \_ 許可權 \_ 寫入、金鑰 \_ 集 \_ 值和金鑰 \_ 建立 \_ 子 \_ 金鑰存取權限。<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

當您呼叫 [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) 函數時，系統會根據金鑰的安全描述項來檢查要求的存取權限。 如果使用者沒有正確的登錄機碼存取權，則開啟作業會失敗。 如果系統管理員需要存取金鑰，解決方案是啟用 SE \_ 取得 \_ 擁有權 \_ 名稱許可權，並使用寫入擁有者存取權開啟登錄機碼 \_ 。 如需詳細資訊，請參閱 [啟用和停用許可權](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)。

\_ \_ 如果您想要讀取或寫入金鑰的系統存取控制清單 (SACL) ，您可以向登錄機碼要求存取系統安全性存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

若要查看金鑰的目前存取權限，包括預先定義的金鑰，請使用登錄編輯程式 (Regedt32.exe) 。 流覽至所需的金鑰之後，請移至 [ **編輯** ] 功能表，然後選取 [ **許可權**]。

 

