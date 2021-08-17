---
description: Windows通訊端2將 Windows 通訊端1.1 的功能延伸到數個區域。 下表摘要說明部分主要功能變更。
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Winsock 程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8451601f92f0fbf7b85532fc5a63479fe2bec26adc1984c74fc1cd7d750a04aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739857"
---
# <a name="winsock-programming-considerations"></a>Winsock 程式設計考慮

Windows通訊端2將 Windows 通訊端1.1 的功能延伸到數個區域。 下表摘要說明部分主要功能變更。



| 功能                                                                                                           | 描述                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows通訊端2架構](windows-sockets-2-architecture-2.md)                                             | Windows 通訊端2架構的描述。                                                                                                                                                                                                                                           |
| [通訊端控制碼](socket-handles-2.md)                                                                             | 通訊端控制碼可以在 Windows 通訊端2中選擇性地做為檔案控制代碼。 您可以使用通訊端控制碼搭配標準的 Windows 檔案 i/o 函數。                                                                                                                                           |
| [同時存取多個傳輸通訊協定](simultaneous-access-to-multiple-transport-protocols-2.md)   | 允許應用程式使用熟悉的通訊端介面，以同時存取數個已安裝的傳輸通訊協定。                                                                                                                                                        |
| [通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)                                 | 包含一組標準化的函式，可用於查詢及使用目前存在的無數名稱解析網域 (例如 DNS、SAP 和 X. 500) 。                                                                                                                                  |
| [通訊協定獨立的多播和 multipoint](protocol-independent-multicast-and-multipoint-2.md)               | 應用程式會探索傳輸所提供的 multipoint 或多播功能類型，並以一般方式使用這些功能。                                                                                                                                                     |
| [重迭 i/o](overlapped-i-o-and-event-objects-2.md)                                                           | 在 Windows 環境中建立的模型之後，將通訊端 i/o 的重迭範例納入。                                                                                                                                                                                   |
| [散佈/收集 i/o](scatter-gather-i-o-2.md)                                                                     | 遵循在 Windows 環境中建立的模型，將散佈/收集功能與通訊端 i/o 的重迭範例合併。                                                                                                                                                 |
| QoS) [的服務品質](flow-specification-quality-of-service-2.md) (                                            | 建立慣例，讓應用程式用來協調頻寬和延遲等參數的必要服務層級。 其他 QoS 相關的增強功能包含網路特定服務延伸品質的機制。                                                         |
| [提供者特定的擴充機制](provider-specific-extension-mechanism-2.md)                               | [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式可讓服務提供者提供提供者特有的功能延伸模組。                                                                                                                                                                           |
| [共用通訊端](shared-sockets-2.md)                                                                             | 引進 [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) 函式，以啟用跨進程的通訊端共用。                                                                                                                                                                       |
| [連接設定和卸載](connection-setup-and-teardown-2.md)                                               | 應用程式可以在決定是否接受連入連線要求之前取得呼叫端資訊，例如呼叫者識別碼和服務品質。 支援此) 的通訊協定也可能 (，以便在連線終止時于端點之間交換使用者資料。 |
| [正常關機、延遲選項和通訊端關閉](graceful-shutdown-linger-options-and-socket-closure-2.md) | 應用程式有數個選項可關閉通訊端連線 (關機順序) 。                                                                                                                                                                                                  |
| [與通訊協定無關的頻外資料](protocol-independent-out-of-band-data-2.md)                               | 資料流程通訊端抽象包括頻外 (OOB) 資料的概念。                                                                                                                                                                                                                   |
| [Debug 和 Trace 設備](debug-and-trace-facilities-2.md)                                                     | Windows通訊端2支援特殊設計的 Ws2 \_32.dll 和個別的 debug/TRACE DLL 版本。                                                                                                                                                                                      |
| [Windows通訊端相容性問題](windows-sockets-compatibility-issues-2.md)                                 | Windows除了處理虛擬封鎖的函式以外，通訊端2繼續支援所有 Windows 通訊端1.1 語義和函式呼叫。                                                                                                                                              |
| [處理 Winsock 錯誤](handling-winsock-errors.md)                                                             | 應用程式如何取出和處理 Winsock 錯誤。                                                                                                                                                                                                                             |



 

 

 



