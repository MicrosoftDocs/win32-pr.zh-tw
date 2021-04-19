---
description: 您無法使用 Certadm.dll 的備份和還原功能來備份憑證服務私密金鑰。
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: 備份和還原憑證服務私密金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891794f36e87b2aa4b6a5d5c8dde55304da20601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974060"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>備份和還原憑證服務私密金鑰

您無法使用 Certadm.dll 的備份和還原功能來備份憑證服務 [*私密金鑰*](../secgloss/p-gly.md)。 這些函式無法備份私密金鑰，因為這些函式的目的是要備份和還原憑證服務資料庫 (以及) 的相關檔案，而且此資料庫不包含任何 (的私密金鑰，即使是) 自我發行的憑證也一樣。

若要備份憑證服務私密金鑰，請使用「憑證授權單位單位」 MMC 嵌入式管理單元，或使用 certutil 命令 (搭配-backup 或-backupkey 指定的) 。 使用「憑證授權單位單位」 MMC 嵌入式管理單元或 certutil 來備份私密金鑰會導致私密金鑰寫入 PKCS 12 檔案中 \# 。 雖然這個 PKCS \# 12 檔案受密碼保護，但它應該被視為非常機密，而且必須安全地儲存; PKCS 12 檔案的密碼 \# 也應受未經授權的人員保護。

同樣地，憑證服務的備份和還原功能無法還原私密金鑰。 PKCS 12 檔案中包含的憑證服務備份金鑰 \# 可以由 [憑證授權單位單位] mmc 嵌入式管理單元來還原，或是由 certutil 命令 (指定-restore 或-restorekey 動詞) 來還原，請注意執行還原作業的人員必須知道 PKCS 12 檔案的密碼 \# 。

只有兩種情況下必須備份憑證服務私密金鑰。 第一個案例是在安裝憑證服務之後。 第二個案例是在憑證服務憑證的任何更新作業之後。

 

 
