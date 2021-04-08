---
title: COM 登錄機碼
description: COM 登錄機碼
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840128"
---
# <a name="com-registry-keys"></a>COM 登錄機碼

登錄包含 COM 所使用的豐富資訊。 最重要的資訊會儲存在下列索引鍵中。



| Key                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | 將設定選項 (一組命名值) ，將一個或多個分散式 COM 物件設定為登錄中的一個位置。 此機碼下的子機碼可用來將應用程式識別碼 (AppID) 對應至遠端伺服器名稱。 為了簡化一般安全性和設定設定的管理，相同可執行檔所裝載的分散式 COM 物件會分組為一個 AppID。<br/>                                                                                                                                                                                                                                                                                                                      |
| [Clsid](clsid-key-hklm.md)<br/>                              |  (CLSID) 的類別識別碼是識別 COM 類別物件的全域唯一識別碼。 如果伺服器或容器允許連結至内嵌物件，請為每個支援的物件類別註冊一個 CLSID。 CLSID 索引鍵包含當類別處於執行中狀態時，預設 COM 處理常式用來傳回其相關資訊的資訊。<br/> 若要取得應用程式的 CLSID，請使用在 COM 工具組的 TOOLs 目錄中找到的 uuidgen.exe， \\ 或使用 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)。 <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               |  (ProgID) 的程式設計識別碼是可以與 CLSID 相關聯的登錄專案。 ProgID 索引鍵會將使用者易記的字串對應至 CLSID。 如同 CLSID，ProgID 會識別類別，但精確度較低。 在無法使用 CLSID 的程式設計情況下使用 ProgID。 Progid 不應該出現在使用者介面中。 Progid 不保證是唯一的，因此只能在不發生名稱衝突的情況下使用。<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | 將 ProgID 與 CLSID 產生關聯。 它是用來判斷物件應用程式的最新版本。 和 ProgID 一樣，與版本無關的 ProgID 可以註冊為人們可讀取的名稱。 <br/> 應用程式必須在 VersionIndependentProgID 索引鍵下註冊與版本無關的程式設計識別碼。 與版本無關的 ProgID 指的是應用程式的類別，而且不會從版本變更為版本，而是在所有版本中都保持不變。 它會與宏語言搭配使用，並參考目前安裝的應用程式類別版本。 與版本無關的 ProgID 必須對應至最新版本的物件應用程式名稱。 <br/> |
| [\_副檔名](-file-extension--key.md)<br/>              | 將副檔名與 ProgID 產生關聯。<br/> 副檔名中包含的資訊是由系統和檔案的 [名字](file-monikers.md)標記所使用。 [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) 使用副檔名來提供相關聯的 CLSID。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [介面](interface-key.md)<br/>                           | 藉由將介面名稱與介面識別碼 (IID) 產生關聯，以註冊新的介面。 它會將 Iid 對應至介面的特定資訊。 大部分的資訊都需要跨進程界限使用介面。 <br/> 當您加入新的介面時，必須完成 COM 的介面機碼才能註冊新的介面。 每個新介面都必須有一個 IID 子機碼。 <br/>                                                                                                                                                                                                                                                                                                       |
| [Ole](hkey-local-machine-software-microsoft-ole.md)<br/>     | 控制分散式 COM 物件的預設啟動和存取權限，以及未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之應用程式的呼叫層級安全性功能。 只有系統管理員可以完整存取登錄的這個部分。 所有其他使用者都具有唯讀存取權。 <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> </dl>

 

 





