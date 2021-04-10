---
title: 備份
description: 允許備份應用程式與其他應用程式和服務進行備份和還原作業的通訊。 執行磁帶備份、初始化磁帶，以及取出磁帶機資訊。 使用儲存 (SIS) 的單一實例存放區來維護重複的檔案。
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- 備份備份
- 備份備份，首頁
- 還原作業備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092955"
---
# <a name="backup"></a>備份

備份和還原的登錄機碼可讓備份應用程式與其他應用程式和服務進行備份和還原作業的通訊。 如需詳細資訊，請參閱 [備份和還原的登錄機碼和值](registry-keys-for-backup-and-restore.md)。

磁帶備份 API 可讓備份應用程式讀取和寫入磁帶、初始化磁帶，以及取出磁帶或磁帶機資訊。 如需詳細資訊，請參閱 [磁帶備份](tape-backup.md)。

單一實例存放區 (SIS) 是一個架構，其設計目的是要以最少的額外負荷來維護重複的檔案。 備份應用程式會使用 SIS 備份 API 來存取 SIS 架構。 如需詳細資訊，請參閱 [單一實例儲存區和 SIS 備份](single-instance-store-and-sis-backup.md)。

加密檔案的備份和還原是由原始加密 API 所啟用，該 API 會讀取和寫入加密的檔案，同時以加密格式保留資料。 API 可讓您備份和還原這些檔案中的加密資料，同時符合維護已備份資料之安全性的目標，並可供缺乏在檔案上使用加密金鑰之許可權的應用程式使用。 如需詳細資訊，請參閱 [備份和還原加密的](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)檔案。

Srdelayed 工具可以讓系統狀態修復應用程式移動、刪除和設定系統檔案的簡短名稱。 如需詳細資訊，請參閱 [Srdelayed.exe](srdelayed-exe.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[備份參考](backup-reference.md)
</dt> </dl>

 

 