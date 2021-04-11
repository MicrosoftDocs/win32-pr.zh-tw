---
title: 儲存使用者特定資訊
description: 應用程式應在使用者特定位置中 儲存使用者專屬資訊 ，藉此與套用到所有使用者的全域資訊區隔。
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023640"
---
# <a name="storing-user-specific-information"></a>儲存使用者特定資訊

在遠端桌面服務環境中，應用程式應該將使用者特定的資訊儲存在使用者特定的位置，與套用至所有使用者的全域資訊分開。 這項規則適用于儲存在登錄中的資訊，以及儲存在檔案中的資訊。 一般情況下，請不要假設一部電腦相當於一位使用者。

在 **HKEY \_ CURRENT \_ user** 登錄機碼下儲存使用者特定的登錄資訊。 遠端桌面服務當使用者登入時，會將目前使用者的個人登錄區載入 **HKEY 的 \_ 目前 \_ 使用者** 。 當然，遠端桌面服務管理登錄，以確保每個登入的用戶端在 **HKEY \_ CURRENT \_ user** 下偵測到正確的使用者 hive。 如需登錄機碼的詳細資訊，請參閱登錄機[碼安全性和存取權限](/windows/desktop/SysInfo/registry-key-security-and-access-rights)和登錄[hive。](/windows/desktop/SysInfo/registry-hives)

相反地，所有使用者都會共用 **HKEY \_ 本機 \_ 電腦** hive。 使用 **HKEY \_ 本機 \_ 電腦** 來儲存電腦特定的資訊，而不是使用者特定的資訊。

將使用者喜好設定檔案或其他使用者專屬檔案儲存在使用者的根目錄或使用者指定的目錄中。 此考慮適用于用來儲存暫存資訊的暫存檔案 (例如快取的資料) ，或將資料傳遞至另一個應用程式。 使用者特定的暫存檔案也必須以個別使用者的方式儲存。

您可以使用 [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) 函式搭配 CSIDL \_ 個人旗標，以取得使用者個人檔案目錄的位置。 您也可以使用 [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) 函式來取出 Windows 目錄的路徑。 在遠端桌面服務環境中，Windows 目錄保證每個使用者都是私用的。 請勿將使用者專屬的檔案儲存在系統目錄（例如 WINDOWS）下，或程式目錄（例如 Program Files）下。

為了避免使用者的資訊和喜好設定之間的衝突，應用程式應該將每位使用者的暫存資訊儲存在使用者特定的暫存檔案中。 使用者專屬的暫存檔案也會防止因檔案鎖定衝突而造成的應用程式失敗。 若要指定儲存暫存資訊的路徑，請使用 [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) 函數。

 

 