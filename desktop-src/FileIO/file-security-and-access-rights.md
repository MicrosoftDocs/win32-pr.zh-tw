---
description: 由於檔案是安全的物件，因此對它們的存取會受到控制 Windows 中所有其他安全物件存取權的存取控制模型所管制。
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: 檔案安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971721"
---
# <a name="file-security-and-access-rights"></a>檔案安全性與存取權限

由於檔案是 [安全的物件](/windows/desktop/SecAuthZ/securable-objects)，因此對它們的存取會受到控制 Windows 中所有其他安全物件存取權的存取控制模型所管制。 如需此模型的詳細說明，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。

當您呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)、 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)或 [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)函數時，可以指定檔案或目錄的 [安全描述項](/windows/desktop/api/winnt/ns-winnt-security_descriptor)。 如果您對 *lpSecurityAttributes* 參數指定 **Null** ，則檔案或目錄會取得預設安全描述項。 存取控制會在檔案或目錄的預設安全描述項中， (ACL) 清單繼承自其父目錄。 請注意，只有在新建立檔案或目錄時，才會指派預設安全描述項，而不會在重新命名或移動時指派。

若要取得檔案或目錄物件的安全描述項，請呼叫 [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要變更檔案或目錄物件的安全描述項，請呼叫 [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) 或 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

檔案和目錄的有效存取權限包括 **刪除**、**讀取 \_ 控制**、**寫入 \_ DAC**、**寫入 \_ 擁有** 者，以及 **同步處理**[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。 檔案 [**存取權限常數**](file-access-rights-constants.md) 中的表格會列出檔案和目錄的特定存取權限。

雖然 **同步** 存取許可權是在 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) 清單中定義為在其中一個等候函式中指定檔案控制代碼的許可權，但在使用非同步檔案 i/o 作業時，您應該等候已 [**正確設定之**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 重迭結構中所包含的事件控制碼，而不是使用檔案控制代碼與同步處理的 **同步** 存取許可權。

以下是檔案和目錄的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。



<table>
<thead>
<tr class="header">
<th>存取權限</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>同步</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>同步</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>同步</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows 會將要求的存取權限和執行緒存取權杖中的資訊，與檔案或目錄物件的安全描述項中的資訊進行比較。 如果比較不禁止授與所有要求的存取權限，則會將物件的控制碼傳回給執行緒，並授與存取權限。 如需此程式的詳細資訊，請參閱 [執行緒和安全物件之間的互動](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects)。

依預設，存取檔案或目錄的授權是由與該檔案或目錄相關聯之安全描述項中的 Acl 所控制。 尤其是，父目錄的安全描述項不會用來控制對任何子檔案或目錄的存取。 您可以藉由移除使用者的 **略過 \_ 遍歷 \_ 檢查**[許可權](/windows/desktop/SecAuthZ/privileges)，來強制執行檔案 **\_ 遍歷**[訪問](/windows/desktop/SecAuthZ/access-rights-and-access-masks)許可權。 在一般情況下，並不建議這麼做，因為許多程式都不會正確處理目錄遍歷錯誤。 檔案的主要用途是在目錄上 **進行存取權限 \_** 的主要用途，是在需要與 Unix 系統之間的互通性時，能夠符合某些 IEEE 和 ISO POSIX 標準。

Windows 安全性模型提供一種方式，讓子目錄繼承或防止繼承父目錄的安全描述項中的一或多個 Ace。 每個 ACE 都包含決定如何繼承的資訊，以及它是否會影響繼承目錄物件。 例如，某些繼承的 Ace 會控制繼承的目錄物件的存取，而這些 Ace 稱為 *有效的 ace*。 所有其他 Ace 都稱為 *僅限繼承 ace*。

Windows 安全性模型也會根據 [ace 繼承規則](/windows/desktop/SecAuthZ/ace-inheritance-rules)，強制將 ace 自動繼承到子物件。 此自動繼承以及每個 ACE 中的繼承資訊，會決定如何將安全性限制傳遞到目錄階層。

請注意，您不能使用拒絕存取的 ACE 來拒絕檔案的 **一般 \_ 讀取** 或僅 **一般 \_ 寫入** 存取權。 這是因為對於檔案物件而言， **泛型 \_ 讀取** 或 **一般 \_ 寫入** 的泛型對應會包含 **同步** 存取許可權。 如果 ACE 拒絕對信任者的 **一般 \_ 寫入** 存取，而信任者要求 **一般 \_ 讀取** 許可權，則要求將會失敗，因為要求會隱含地包含 ACE 隱含拒絕的 **同步** 存取，反之亦然。 請使用允許存取的 Ace 明確地允許允許的存取權限，而不是使用拒絕存取的 Ace。

管理儲存體物件存取的另一種方式是加密。 在 Windows 中執行檔案系統加密是加密檔案系統（EFS）。 EFS 只會加密檔案而非目錄。 加密的優點是，它可為套用在媒體上的檔案提供額外的保護，而不是透過檔案系統和標準的 Windows 存取控制架構。 如需檔案加密的詳細資訊，請參閱檔案 [加密](file-encryption.md)。

在大部分的情況下，讀取和寫入檔案或目錄物件之安全性設定的功能，會限制為核心模式進程。 很明顯地，您不希望任何使用者進程都能變更私人檔案或目錄的擁有權或存取限制。 但是，如果您在檔案或目錄上放置的存取限制不允許應用程式的使用者模式進程讀取，則備份應用程式無法完成其備份檔案的作業。 備份應用程式必須能夠覆寫檔案和目錄物件的安全性設定，以確保完整備份。 同樣地，如果備份應用程式嘗試透過磁片常駐複本來寫入檔案的備份副本，而您明確拒絕備份應用程式處理常式的寫入權限，則還原作業無法完成。 在此情況下，備份應用程式也必須能夠覆寫檔案的存取控制設定。

「 **Se \_ 備份 \_ 名稱** 」和「 **se \_ 還原 \_ 名稱** 」存取權限是特別建立來提供備份應用程式的能力。 如果已在備份應用程式處理常式的存取權杖中授與並啟用這些許可權，則可以呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 開啟您的檔案或目錄進行備份，並將標準的 **讀取 \_ 控制** 存取權指定為 *dwDesiredAccess* 參數的值。 不過，若要將呼叫進程識別為備份程式，呼叫 **CreateFile** 必須在 *dwFlagsAndAttributes* 參數中包含檔案 **旗標 \_ \_ 備份 \_ 語義** 旗標。 函式呼叫的完整語法如下所示：


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



這可讓備份應用程式進程開啟您的檔案，並覆寫標準安全性檢查。 若要還原您的檔案，在開啟要寫入的檔案時，備份應用程式會使用下列 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 呼叫語法。


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



在某些情況下，備份應用程式必須能夠變更檔案或目錄的存取控制設定。 例如，當檔案或目錄之磁片常駐複本的存取控制設定與備份複本不同時。 如果在備份檔案案或目錄之後變更這些設定，或已損毀，就會發生這種情況。

對 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的呼叫中指定的檔案 **\_ 旗標 \_ 備份 \_ 語義** 旗標，會提供備份應用程式處理許可權，以讀取檔案或目錄的存取控制設定。 有了這個許可權之後，備份應用程式進程就可以呼叫 [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) 和 [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) ，以讀取和重設存取控制設定。

如果備份應用程式必須具有系統層級 [存取控制設定](/windows/desktop/SecAuthZ/access-control-lists)的存取權，則必須在傳遞至 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的 *dwDesiredAccess* 參數值中指定「**存取 \_ 系統」 \_ 安全性** 旗標。

備份應用程式會呼叫 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ，以讀取為還原作業指定的檔案和目錄，並 [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) 寫入這些檔案和目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
