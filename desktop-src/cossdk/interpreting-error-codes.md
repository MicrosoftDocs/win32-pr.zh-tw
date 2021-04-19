---
description: 解讀錯誤碼
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: 解讀錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973163"
---
# <a name="interpreting-error-codes"></a>解讀錯誤碼

判斷出哪個應用程式是問題的來源之後，您需要找出發生了哪些錯誤。 根據您的應用程式所使用的語言，會以不同的格式引發並報告錯誤。

在 Microsoft Visual C++ 中，成功、警告和失敗值會使用稱為 **HRESULT** 的32位數位傳回。 如需系統定義的 **HRESULT** 值清單，請參閱 Windows SDK 隨附的標頭檔 winerror.h。 此檔案包含所有 COM + 錯誤碼和描述。 如需 **HRESULT** 值的詳細資訊，請參閱 [錯誤處理](/windows/desktop/com/error-handling-in-com)。

JAVA 語言會擲回 ComFailException 的實例來指出失敗，其中 ComFailException 物件會指定 **HRESULT**。 ComSuccessException 的實例表示成功，傳回值為 False。 如需有關解讀這些例外狀況的詳細資訊，請參閱 Microsoft Visual j + + 檔。

> [!Note]  
> 裝載 Visual j + + 物件的 COM + 應用程式伺服器進程不會閒置 (即使是使用零的作用中物件) ，除非您在 VJ6 IDE 中關閉 JIT 偵錯程式。 如需如何進行的詳細資訊，請參閱 Visual c + + 檔。

 

在 Visual Basic 中，您可以藉由檢查 Err 屬性來取出 **HRESULT** 值。 您可以使用 Err. Description 屬性抓取錯誤的描述。

您也可以在 Microsoft Visual Studio 中使用 ERRLOOK 公用程式來取出系統錯誤訊息或模組錯誤訊息。 如果您在 Visual Studio 偵錯工具或其他啟用自動化的應用程式中，拖放了十六進位或十進位值，ERRLOOK 就會自動捕獲錯誤訊息正文。 您也可以輸入值，方法是在 IDE 剪貼簿中輸入或貼上，然後按一下 [ **查閱** ] 選項。

下列 c + + 方法會根據輸入 **HRESULT** 列印錯誤的描述。


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



下表提供 COM + 中常見錯誤碼的說明。



| 錯誤碼                                                   | 定義                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMADMIN \_ E \_ ALREADYINSTALLED<br/>                      | 物件已經註冊。<br/>                                                                                                                                                                     |
| COMADMIN \_ E \_ 應用程式 \_ 檔 \_ READFAIL<br/>                   | 讀取應用程式檔時發生錯誤。<br/>                                                                                                                                                          |
| COMADMIN \_ 電子 \_ 應用程式 \_ 檔 \_ 版本<br/>                    | 應用程式檔中的版本號碼無效。<br/>                                                                                                                                                           |
| COMADMIN \_ E \_ 應用程式 \_ 檔 \_ WRITEFAIL<br/>                  | 寫入應用程式檔時發生錯誤。<br/>                                                                                                                                                       |
| COMADMIN \_ E \_ APPDIRNOTFOUND<br/>                        | 找不到應用程式安裝目錄。<br/>                                                                                                                                                          |
| COMQC \_ E \_ 應用程式 \_ 未 \_ 排入佇列<br/>                 | 只有標示為「已排入佇列」的 COM + 應用程式才能使用 "queue" 標記來建立。<br/>                                                                                                                      |
| COMADMIN \_ E \_ APPLICATIONEXISTS<br/>                     | 已安裝應用程式。<br/>                                                                                                                                                                 |
| COMADMIN \_ E \_ APPLID \_ 符合 \_ CLSID<br/>                | 此電腦上已安裝具有與新應用程式識別碼相同 GUID 的 CLSID。<br/>                                                                                                            |
| COMADMIN \_ E \_ 應用程式 \_ 未 \_ 執行<br/>                     | 指定的應用程式目前不在執行中。<br/>                                                                                                                                                   |
| COMADMIN \_ E \_ AUTHENTICATIONLEVEL<br/>                   | 無法設定更新要求所需的驗證層級。<br/>                                                                                                                                       |
| COMADMIN \_ E \_ BADPATH<br/>                               | 檔案路徑無效。<br/>                                                                                                                                                                             |
| COMADMIN \_ E \_ BADREGISTRYLIBID<br/>                      | 註冊的類型程式庫識別碼無效。<br/>                                                                                                                                                            |
| COMADMIN \_ E \_ BADREGISTRYPROGID<br/>                     | 元件的 ProgID 遺失或損毀。<br/>                                                                                                                                                         |
| COMADMIN \_ E \_ \_ 無法 \_ 匯出 \_ 應用程式 \_ PROXY<br/>          | 應用程式 proxy 無法匯出。<br/>                                                                                                                                                              |
| COMADMIN \_ E \_ \_ 無法 \_ 啟動 \_ 應用程式<br/>                  | 無法啟動應用程式，因為它可能是程式庫應用程式或應用程式 proxy。<br/>                                                                                                       |
| COMADMIN \_ E \_ \_ 無法 \_ 匯出 \_ SYS \_ 應用程式<br/>            | 系統應用程式無法匯出。<br/>                                                                                                                                                             |
| COMADMIN \_ E \_ \_ 無法訂閱 \_ \_ 元件<br/>        | 使用者無法訂閱這個元件，因為元件可能已匯入。<br/>                                                                                                             |
| COMADMIN \_ E \_ CANTCOPYFILE<br/>                          | 複製檔案時發生錯誤。<br/>                                                                                                                                                                   |
| COMADMIN \_ E \_ CLSIDORIIDMISMATCH<br/>                    | 應用程式檔 Clsid 或 Iid 不符合對應的 Dll。<br/>                                                                                                                                      |
| COMADMIN \_ E \_ 複合 \_ 移動 \_ 不良的 \_ DEST<br/>                 | 元件移動失敗，因為目的地應用程式已不存在。<br/>                                                                                                                       |
| COMADMIN \_ E \_ 複合 \_ 移動已 \_ 鎖定<br/>                    | 不允許移動元件，因為來源或目的地應用程式是系統應用程式，或目前已鎖定變更。<br/>                                                |
| COMADMIN \_ E \_ COMPFILE \_ BADTLB<br/>                      | 無法載入類型程式庫。<br/>                                                                                                                                                                 |
| COMADMIN \_ E \_ COMPFILE \_ CLASSNOTAVAIL<br/>               | DLL 不支援類型程式庫中所列的元件。<br/>                                                                                                                                   |
| COMADMIN \_ E \_ COMPFILE \_ DOESNOTEXIST<br/>                | 此檔案不存在。<br/>                                                                                                                                                                             |
| COMADMIN \_ E \_ COMPFILE \_ GETCLASSOBJ<br/>                 | DLL 中的 [**GetClassObject**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) 方法失敗。<br/>                                                                                                                |
| COMADMIN \_ E \_ COMPFILE \_ LOADDLLFAIL<br/>                 | 無法載入 DLL。<br/>                                                                                                                                                                          |
| COMADMIN \_ E \_ COMPFILE \_ NOREGISTRAR<br/>                 | 無法使用這個檔案中所參考的元件註冊機構。<br/>                                                                                                                                     |
| COMADMIN \_ E \_ COMPFILE \_ NOTINSTALLABLE<br/>              | 檔案不包含元件或元件資訊。<br/>                                                                                                                                        |
| COMADMIN \_ E \_ COREQCOMPINSTALLED<br/>                    | 已安裝相同 DLL 中的元件。<br/>                                                                                                                                                     |
| COMADMIN \_ E \_ DLLLOADFAILED<br/>                         | 無法載入 DLL。<br/>                                                                                                                                                                          |
| COMADMIN \_ E \_ DLLREGISTERSERVER<br/>                     | 安裝元件時， [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 函式失敗。<br/>                                                                                                  |
| COMADMIN \_ E \_ EVENTCLASS \_ \_ 無法成為 \_ 訂閱者<br/>      | 事件類別無法設定為訂閱者元件。 嘗試以事件類別做為訂閱者建立訂閱時，會傳回此錯誤。<br/>                          |
| COMADMIN \_ E \_ INVALIDUSERIDS<br/>                        | 應用程式檔中有一或多個使用者無效。<br/>                                                                                                                                              |
| COMADMIN \_ E \_ KEYMISSING<br/>                            | 在目錄中找不到物件。<br/>                                                                                                                                                              |
| COMADMIN \_ E \_ LIB \_ 應用程式 \_ PROXY \_ 不相容<br/>         | 程式庫應用程式和應用程式 proxy 不相容。 嘗試匯出應用程式 proxy，而應用程式的啟用屬性是程式庫時，會傳回此錯誤。 <br/> |
| COMADMIN \_ E \_ NOREGISTRYCLSID<br/>                       | 元件的 CLSID 遺失或已損毀。<br/>                                                                                                                                                          |
| COMADMIN \_ E \_ NOSERVERSHARE<br/>                         | 沒有任何可用的伺服器檔案共用。<br/>                                                                                                                                                                    |
| COMADMIN \_ E \_ NOTCHANGEABLE<br/>                         | 此物件及其子物件的變更已停用。<br/>                                                                                                                                        |
| COMADMIN \_ E \_ NOTDELETEABLE<br/>                         | 已停用此物件的 delete 函數。<br/>                                                                                                                                                |
| COMADMIN \_ E \_ NOTINREGISTRY<br/>                         | 在登錄中找不到物件。<br/>                                                                                                                                                                     |
| COMADMIN \_ E \_ NOUSER<br/>                                | 一或多個使用者無效。<br/>                                                                                                                                                                      |
| COMADMIN \_ E \_ 物件 \_ 不 \_ \_ 存在<br/>              | 找不到其中一個指定的物件。<br/>                                                                                                                                                         |
| \_缺少 COMADMIN E \_ 物件 \_ 父系 \_<br/>               | 其中一個要插入或更新的物件不屬於有效的父集合。<br/>                                                                                                            |
| COMADMIN \_ E \_ OBJECTERRORS<br/>                          | 存取一或多個物件時發生錯誤。 如需詳細資訊，請參閱 [**ErrorInfo**](errorinfo.md) 集合。<br/>                                                                               |
| COMADMIN \_ E \_ OBJECTEXISTS<br/>                          | 您嘗試新增或重新命名的物件已經存在。<br/>                                                                                                                                        |
| COMADMIN \_ E \_ OBJECTINVALID<br/>                         | 物件的一或多個屬性遺失或無效。<br/>                                                                                                                                        |
| COMADMIN \_ E \_ OBJECTNOTPOOLABLE<br/>                     | 此物件無法共用。<br/>                                                                                                                                                                      |
| COMADMIN \_ E \_ PROPERTYSAVEFAILED<br/>                    | 一或多個屬性設定無效或彼此衝突。<br/>                                                                                                                      |
| COMADMIN \_ E \_ 屬性 \_ 溢位<br/>                    | 屬性值太大。<br/>                                                                                                                                                                      |
| COMADMIN \_ E \_ REGFILE \_ 已損毀<br/>                      | 註冊檔案已損毀。<br/>                                                                                                                                                                     |
| COMADMIN \_ E \_ REGISTERTLB<br/>                           | 系統無法註冊類型程式庫。<br/>                                                                                                                                                   |
| COMADMIN \_ E \_ REGISTRARFAILED<br/>                       | 元件註冊機構中發生錯誤。<br/>                                                                                                                                                     |
| COMADMIN \_ E \_ REMOTEINTERFACE<br/>                       | 介面資訊遺失或變更。<br/>                                                                                                                                                   |
| COMADMIN \_ E \_ 需要 \_ 不同的 \_ 平臺<br/>         | 此平臺上未啟用這項操作。<br/>                                                                                                                                                       |
| COMADMIN \_ E \_ 角色 \_ 不 \_ \_ 存在<br/>                | 指派給元件、介面或方法的角色不存在於應用程式中。<br/>                                                                                                               |
| COMADMIN \_ E \_ ROLEEXISTS<br/>                            | 此角色已經存在。<br/>                                                                                                                                                                              |
| COMADMIN \_ E \_ SERVICENOTINSTALLED<br/>                   | 未安裝服務。<br/>                                                                                                                                                                         |
| COMADMIN \_ 電子 \_ 會話<br/>                               | 不支援伺服器目錄版本。<br/>                                                                                                                                                          |
| COMADMIN \_ S \_ SOMEALREADYPAUSED<br/>                     | 一或多個指定的應用程式進程已經暫停。<br/>                                                                                                                               |
| COMADMIN \_ S \_ SOMEALREADYRUNNING<br/>                    | 一或多個指定的應用程式進程已在執行中。<br/>                                                                                                                              |
| COMADMIN \_ E \_ 啟動 \_ 應用程式 \_ 需求 \_ 元件<br/>         | 若要啟動應用程式，您必須在應用程式中有元件。<br/>                                                                                                                                 |
| COMADMIN \_ E \_ SVCAPP \_ NOT \_ 共用 \_ 或 \_ 可回收<br/> | 以 NT 服務的形式執行的 COM + 應用程式可能不會標示為已集區或回收。<br/>                                                                                                               |
| COMADMIN \_ E \_ SYSTEMAPP<br/>                             | 無法在系統應用程式上執行此操作。<br/>                                                                                                                                         |
| COMADMIN \_ E \_ USER \_ IN \_ SET<br/>                         | 已將一或多個使用者指派給本機資料分割集。<br/>                                                                                                                                      |
| COMADMIN \_ E \_ USERPASSWDNOTVALID<br/>                    | 在應用程式上設定的身分識別或密碼無效。<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[找出錯誤的來源](finding-the-source-of-an-error.md)
</dt> <dt>

[COM + 如何修改傳回值](how-com--modifies-return-values.md)
</dt> <dt>

[在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[疑難排解](troubleshooting-the-com--crm.md)
</dt> </dl>

 

