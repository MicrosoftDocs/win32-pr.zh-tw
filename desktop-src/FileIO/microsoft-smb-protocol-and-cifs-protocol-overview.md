---
description: 描述 Microsoft 如何將 Server Message Block (SMB) 通訊協定的執行。
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Microsoft SMB 通訊協定和 CIFS 通訊協定總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943387"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Microsoft SMB 通訊協定和 CIFS 通訊協定總覽

伺服器訊息區 (SMB) 通訊協定是一個網路檔案共用通訊協定，在 Microsoft Windows 中實作為實作為 Microsoft SMB 通訊協定。 定義特定通訊協定版本的訊息封包集會稱為方言。 Common Internet File System (CIFS) Protocol 是 SMB 的用語。 SMB 和 CIFS 也可在 VM、數個 Unix 版本和其他作業系統上使用。

您可以從 [Common Internet File System (cifs) 檔案存取通訊協定](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b)的 MICROSOFT CORPORATION 取得 CIFS 的技術參考。

雖然它的主要目的是檔案共用，但其他 Microsoft SMB 通訊協定功能包含下列各項：

-   [方言協商](microsoft-smb-protocol-dialects.md)
-   判斷網路上或網路流覽的其他 Microsoft SMB 通訊協定伺服器
-   透過網路列印
-   [檔案、目錄和共用存取驗證](microsoft-smb-protocol-authentication.md)
-   檔案和記錄鎖定
-   檔案和目錄變更通知
-   擴充檔案屬性處理
-   Unicode 支援
-   [隨機鎖定](opportunistic-locks.md)

在 OSI 網路模型中，Microsoft SMB 通訊協定最常用於應用層或展示層通訊協定，而且依賴較低層級的通訊協定來進行傳輸。 Microsoft SMB 通訊協定最常使用的傳輸層通訊協定是 NetBIOS over TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))) 。 不過，您也可以在不使用個別傳輸通訊協定的情況下使用 Microsoft SMB 通訊協定。 Microsoft SMB 通訊協定/NBT 組合通常用於回溯相容性。

Microsoft SMB 通訊協定是一種用戶端-伺服器的執行方式，是由一組資料封包所組成，每個封包都包含用戶端傳送的要求，或由伺服器傳送的回應。 這些封包可以廣泛分類，如下所示：

-   會話控制封包會建立並停止共用伺服器資源的連接。
-   檔案存取封包會存取和操作遠端伺服器上的檔案和目錄。
-   一般訊息封包會將資料傳送到列印佇列、mailslots 和具名管道，以及提供有關列印佇列狀態的資料。

某些訊息封包可能會在一次傳輸中分組並傳送，以降低回應延遲並增加網路頻寬。 這稱為「批次處理」。 [MICROSOFT Smb 通訊協定封包交換案例](microsoft-smb-protocol-packet-exchange-scenario.md)一節說明使用封包批次處理的 Microsoft Smb 通訊協定會話範例。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                             | 描述                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft SMB 通訊協定方言](microsoft-smb-protocol-dialects.md)<br/>                                 | 若要使用 Microsoft SMB 通訊協定在用戶端與伺服器之間建立連線，您必須先使用用戶端和伺服器支援的最高層級功能來判斷方言。<br/>                                                      |
| [Microsoft SMB 通訊協定驗證](microsoft-smb-protocol-authentication.md)<br/>                     | Microsoft SMB 通訊協定中使用的安全性模型與其他 SMB 變數所使用的模型相同，且包含兩個層級的安全性使用者和共用。 共用是可由 Microsoft SMB 通訊協定用戶端存取的檔案、目錄或印表機。<br/> |
| [Microsoft SMB 通訊協定封包交換案例](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | 用戶端與伺服器之間的 Microsoft SMB 通訊協定封包交換範例。<br/>                                                                                                                                                                               |



 

 

