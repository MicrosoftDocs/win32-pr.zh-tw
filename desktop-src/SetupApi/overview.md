---
description: " (API) 的設定應用程式開發介面提供一組功能，讓您的安裝應用程式可以呼叫這些函式來執行安裝作業。 這些安裝函式適用于 Windows INF 檔案，以提供下列安裝程式功能。"
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: 概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b6ae457023dff36bfdaf97275c8309bfcfc5c0a12b209dac1921d1a7479940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965104"
---
# <a name="overview"></a>概觀

 (API) 的設定應用程式開發介面提供一組功能，讓您的安裝應用程式可以呼叫這些函式來執行安裝作業。 這些安裝函式適用于 Windows INF 檔案，以提供下列安裝程式功能。



| 如需下列資訊                       | 請參閱                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 佇列檔                               | [檔案佇列](file-queues.md)                                                                                                                                              |
| 安裝檔案                            | [檔案佇列](file-queues.md)<br/> [設定應用程式](setup-applications.md)<br/> [建立安裝程式應用程式](creating-setup-applications.md)<br/> |
| 處理錯誤並提示媒體     | [磁片提示和錯誤處理](disk-prompting-and-error-handling.md)                                                                                                  |
| 更新登錄專案                   | [設定應用程式](setup-applications.md)                                                                                                                                |
| 記錄已安裝的檔案                     | [檔案記錄檔](file-log.md)                                                                                                                                                    |
| 儲存最近使用的來源路徑 | [MRU 來源清單](mru-source-list.md)                                                                                                                                      |



 

Unicode 和 ANSI 版本適用于大部分的設定函數。 Unicode 文字檔應該包含標準0xFEFF 位元組順序標記，才能讓安裝函式將檔案識別為 Unicode 文字。

雖然安裝程式 API 支援提示輸入新的媒體和基本的錯誤處理對話方塊，但安裝函式不會提供 wizard 功能或一般使用者介面。

開發人員應考慮是否可以使用[Windows Installer](/windows/desktop/Msi/windows-installer-portal)安裝其應用程式，而不是安裝程式 API。 Windows安裝程式可讓客戶有效率地安裝及設定您的產品和應用程式，以降低客戶的擁有權總成本 (TCO) 。 安裝程式也可以為您的產品提供新功能，以在不安裝的情況下通告功能、隨選安裝產品，以及新增使用者自訂。

 

