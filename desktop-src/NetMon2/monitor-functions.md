---
description: 本節說明可用來開發自訂監視的 helper 函數。
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: 監視函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677098"
---
# <a name="monitor-functions"></a>監視函式

本節說明可用來開發自訂監視的 helper 函數。



| 函式                                       | 描述                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | 建立監視的實例。                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | 將 HTML CP \_ UTF8 版本字串轉換成 Unicode。                                                                                                             |
| [LoadDWORD](loaddword.md)                     | 從 HTML 設定字串載入 **DWORD** 。                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | 從 HTML TEXTAREA 設定字串載入 IP 位址清單。                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | 從 HTML TEXTAREA 設定字串載入 IPX 地址清單。                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | 從 HTML TEXTAREA 設定字串載入 MAC 地址清單。                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | 將字串 (例如 "157.54.32.45" ) 轉換為 **DWORD** 位址。                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | 在設定字串中搜尋要求的變數名稱，並使用 **HeapAllocMemory**) 來儲存、複製和傳回，以配置足夠的空間 (。 |
| [OnLoadingDLL](onloadingdll.md)               | 表示已開始載入 DLL。 當 MCSVC 第一次載入監視器 DLL 時，會呼叫此函式。                                                     |



 

 

 



