---
title: 呼叫 SRSetRestorePoint
description: 應用程式可以先建立還原點，然後才會造成重大的系統變更，例如安裝、卸載或功能更新。
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592208"
---
# <a name="calling-srsetrestorepoint"></a>呼叫 SRSetRestorePoint

應用程式可以先建立還原點，然後才會造成重大的系統變更，例如安裝、卸載或功能更新。

安裝程式應在安裝之前建立還原點，方法是呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa)函式，並將 [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa)結構的 **DWEVENTTYPE** 成員設定為 [開始 \_ 系統 \_ 變更]。 若要通知系統還原安裝已完成，請呼叫 **SRSetRestorePoint** ，並將 **dwEventType** 設定為 [結束 \_ 系統變更] \_ 。

如果使用者取消應用程式安裝，安裝程式可能會移除安裝開始時所建立的還原點。 移除還原點是選擇性的，可防止使用者在取消時，從安裝程式所進行的非不慎變更中復原。 如果安裝程式要移除還原點，則可以呼叫 [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) 函式，或呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 並將 **dwRestorePointType** 設定為取消作業 \_ 、將 **dwEventType** 設定為 \_ [結束系統變更] \_ ，並將 **llSequenceNumber** 設定為初始呼叫 **SRSetRestorePoint** 所傳回的值。

* * Windows 8： * *

新的登錄機碼可讓應用程式開發人員變更還原點建立的頻率。

應用程式應該建立此金鑰來使用它，因為它不會在系統中之外。 如果機碼不存在，則預設會套用下列各項。 如果應用程式呼叫 **SRSetRestorePoint** 函式來建立還原點，Windows 會在過去24小時內建立任何還原點時，略過建立這個新的還原點。 系統還原將 [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus)結構的 **IISequenceNumber** 成員設定為先前在當日建立之還原點的序號，並將 **nStatus** 成員的值設定為「**錯誤 \_ 成功**」。 **SRSetRestorePoint** 函數會傳回 **TRUE**。

開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **SystemRestorePointCreationFrequency** 。 此登錄機碼的值可以變更還原點建立的頻率。 此登錄機碼的值可以變更還原點建立的頻率。

如果應用程式呼叫 **SRSetRestorePoint** 來建立還原點，而登錄機碼值為0，則系統還原不會略過建立新的還原點。

如果應用程式呼叫 **SRSetRestorePoint** 來建立還原點，而登錄機碼值是整數 n，則系統還原會在前 N 分鐘內建立任何還原點時，略過建立新的還原點。

* * Windows 8： * *

在 Windows 8 上執行的系統還原會監視只與系統還原相關的開機磁碟區中的檔案。 如果之後是由舊版的 Windows 公開快照集，則可能會刪除 Windows 8 上執行系統還原所建立之開機磁碟區的快照集。 請注意，雖然只有一個系統磁碟區，但多重開機系統中的每個作業系統都有一個開機磁碟區。

開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **ScopeSnapshots** 。 如果此登錄機碼值為0，系統還原會以與舊版 Windows 相同的方式，建立開機磁碟區的快照。 如果刪除此值，系統還原在 Windows 8 上執行時，會繼續建立快照集，以監視只與系統還原相關的開機磁碟區中的檔案。

如需範例，請參閱 [使用系統還原](using-system-restore.md)。

 

 




