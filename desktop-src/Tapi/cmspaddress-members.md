---
description: 下列清單包含 CMSP 位址成員。
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: CMSPAddress 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853084"
---
# <a name="cmspaddress-members"></a>CMSPAddress 成員



| 成員類型                    | Name                    | 描述                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Iunknown                        | \*m \_ pFTM               | 無限制執行緒封送處理器的指標。                                                         |
| HANDLE                          | m \_ htEvent              | Tapi3.dll 的事件的控制碼，可用來通知 TAPI 要將資料傳送給它。 |
| 清單 \_ 專案                     | m \_ EventList            | 事件的清單。                                                                                  |
| CMSPCritSection                 | m \_ EventDataLock        | 使用 TAPI 保護與事件處理相關之資料的鎖定。                             |
| ITTerminalManager               | \*m \_ pITTerminalManager | 終端機管理員物件的指標。                                                      |
| CMSPArray <ITTerminal \*> | m \_ 終端機            | 可以在位址上使用的靜態終端機清單。                                    |
| BOOL                            | m \_ fTerminalsUpToDate   | 如果終端機清單是最新的，則此旗標為 **TRUE** 。                                        |
| CMSPCritSection                 | m \_ TerminalDataLock     | 保護終端機相關資料成員的鎖定。                                        |



 

 

 



