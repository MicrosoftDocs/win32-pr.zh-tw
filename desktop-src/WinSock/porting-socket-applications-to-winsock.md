---
description: 本節說明 Winsock 移植考慮。
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: 將通訊端應用程式移植到 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979730"
---
# <a name="porting-socket-applications-to-winsock"></a>將通訊端應用程式移植到 Winsock

本節說明 Winsock 移植考慮。

由於 Microsoft Windows 環境中的執行問題，Windows 通訊端已有少數的實例，而這些實例的範圍嚴格遵循 Berkeley 慣例。

當 Windows 通訊端中發生 Berkeley 慣例的偏差時，就會明確且明確地注明偏差。 例如，如果函式是 Windows 通訊端的特定函式，則會使用與下列類似的函數描述中的片語來指定偏差：

函 **\[ 式名稱 \] 函式** 是 Microsoft 特定的 WINDOWS 通訊端 2 API 擴充功能。

本節提供將 Berkeley (BSD) UNIX 通訊端應用程式移植到 Winsock 的相關資訊：

-   [通訊端資料類型](socket-data-type-2.md)
-   [Select、FD \_ SET 和 FD \_ XXX 宏](select-and-fd---2.md)
-   [錯誤碼-errno、h \_ errno 和 WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [指標](pointers-2.md)
-   [重新命名的函式](renamed-functions-2.md)
-   [支援的通訊端數目上限](maximum-number-of-sockets-supported-2.md)
-   [包含檔案](include-files-2.md)
-   [函數失敗時傳回值](return-values-on-function-failure-2.md)
-   [原始通訊端](service-provided-raw-sockets-2.md)
-   [位元組順序](byte-ordering-2.md)
-   [擴充 Byte-Order 轉換常式](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理 Winsock 錯誤](handling-winsock-errors.md)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows 通訊端錯誤碼](windows-sockets-error-codes-2.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 



