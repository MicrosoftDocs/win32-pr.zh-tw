---
description: 以下是與 Windows Vista 和 Windows Server 2008 中引進的各種檔案系統和安全性功能正確互通的提示。
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: 使用檔案系統和安全性功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113156"
---
# <a name="working-with-file-system-and-security-features"></a>使用檔案系統和安全性功能

以下是與 Windows Vista 和 Windows Server 2008 中引進的各種檔案系統和安全性功能正確互通的提示。

## <a name="interoperability-with-transactions"></a>與交易互通性

為了支援交易，VSS 可確保核心交易管理員 (KTM) 和分散式交易協調器 (DTC) 在建立磁片區陰影複製之前已凍結。 如果系統無法凍結或解除凍結 KTM 或 DTC， [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法可能會傳回下列逾時錯誤：

<dl> VSS \_ E \_ 交易 \_ 凍結 \_ 超時  
VSS \_ E \_ 交易 \_ 解除凍結 \_ 超時  
</dl>

如果要求者收到上述其中一個錯誤碼，則必須重試建立陰影複製。

登錄和檔案系統作業也可以進行交易。 在登錄的案例中，登錄寫入器負責確保交易一致性。 如果是交易式 NTFS (TxF) 檔案系統作業，系統提供者負責確保交易一致性。 完成此作業的方法是在建立陰影複製時，將其裝載為讀取/寫入，以允許自動復原。 在自動復原階段，KTM 會復原任何未完成的交易。

## <a name="identifying-and-creating-hard-links"></a>識別和建立永久連結

備份檔案時，備份應用程式必須識別每個檔案的所有硬連結，以避免備份相同的檔案一次以上。 有兩個新函數可用於列舉永久連結： [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew)。

同樣地，在還原檔案時，備份應用程式必須使用 [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) 函式來還原永久連結。

備份應用程式也必須在 \_ \_ 備份階段和 se 還原名稱中判斷提示「se 備份名稱」許可權，然後在 \_ \_ 還原階段進行。

## <a name="permissions-and-privileges-required-by-backup-applications"></a>備份應用程式所需的許可權和許可權

還原系統檔案的備份應用程式需要下列許可權：

<dl> SE \_ 備份 \_ 名稱  
SE \_ 還原 \_ 名稱  
SE \_ 安全性 \_ 名稱  
SE \_ 取得 \_ 擁有權 \_ 名稱  
</dl>

備份應用程式也必須在 \_ 還原階段要求寫入擁有者存取權。

## <a name="windows-media-digital-rights-management"></a>Windows Media 數位 Rights Management

Windows Media 數位 Rights Management (DRM) 用戶端會在% ProgramData% \\ Microsoft \\ Windows DRM 目錄中維護敏感性狀態和授權檔案的目錄 \\ 。 此目錄中的檔案應該與暫存和快取檔案同時進行清除。 若要確保 Windows DRM 用戶端維持一致的狀態，您必須避免備份或還原這些檔案。 此目錄列在 FilesNotToBackup 登錄機碼中。 如需 FilesNotToBackup 索引鍵的詳細資訊，請參閱 [產生備份組](generating-a-backup-set.md)。

## <a name="user-account-control"></a>使用者帳戶控制

在 Windows Vista 中引進 (UAC) 的使用者帳戶控制，表示除非另有指定，否則應用程式必須在標準使用者帳戶下執行。 此外，UAC 的檔案和登錄虛擬化功能會改變儲存使用者資料的位置。 如需如何使用 UAC 和檔案和登錄虛擬化的詳細資訊，請參閱下列參考：

<dl>

[Windows Vista 和 Windows Server 2008 開發人員故事： Windows Vista 應用程式開發需求適用于使用者帳戶控制 (UAC) ](/previous-versions/aa905330(v=msdn.10))  
[使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[ (UAC) 修補的使用者帳戶控制](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>BitLocker 磁碟機加密

BitLocker 磁碟機加密是 Windows Vista Enterprise、Windows Vista 旗艦版以及 Windows Server 2008 中的一項新功能，可提供安全的啟動和完整磁片區加密。 瞭解這項功能對於執行離線還原的備份應用程式開發人員而言很重要，因為可能需要將資料還原至加密的磁片磁碟機。

若要將資料還原至加密的磁片磁碟機，請執行下列步驟：

1.  解除鎖定磁片磁碟機。
2.  關閉 BitLocker 磁碟機加密。
3.  執行還原。
4.  開機進入還原的作業系統，然後開啟 BitLocker 磁碟機加密。

如需有關 BitLocker 磁碟機加密的詳細資訊（包括逐步指南），請參閱 Microsoft TechNet Windows Vista 網站上的 [BitLocker 磁碟機加密](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) 。 如需 BitLocker 磁碟機加密 WMI 提供者的詳細資訊，請參閱 [BitLocker 磁碟機加密提供者](../secprov/bitlocker-drive-encryption-provider.md)。

 

 
