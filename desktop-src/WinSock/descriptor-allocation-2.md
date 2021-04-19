---
description: 雖然 Windows 通訊端服務提供者建議將通訊端實作為可安裝的檔案系統 (IFS) 物件，但 Winsock 架構也可容納其通訊端控制碼不是 IFS 物件的服務提供者。
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: 描述項配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970809"
---
# <a name="descriptor-allocation"></a>描述項配置

雖然 Windows 通訊端服務提供者建議將通訊端實作為可安裝的檔案系統 (IFS) 物件，但 Winsock 架構也可容納其通訊端控制碼不是 IFS 物件的服務提供者。 具有 IFS 處理常式的提供者會透過 \_ \_ [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中的 XP1 IFS handles 屬性位來指出這一點。  (注意： \_ \_ API 規格的發行2.0.8 中未包含 XP1 的 IFS 控制碼屬性位，但已透過勘誤機制新增。 ) Winsock SPI 用戶端可能會利用這些描述項搭配標準 Windows i/o 設備（例如 [ReadFile](/windows/win32/api/fileapi/nf-fileapi-readfile) 和 [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile)）使用這些描述元，來利用其通訊端描述項為 IFS 控制碼的提供者。

每當 IFS 提供者建立新的通訊端描述項時，提供者在提供新的 Windows 通訊端 SPI 用戶端的控制碼之前，都必須先呼叫 [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) 。 此函式會從提供者取得提供者識別碼和建議的 IFS 控制碼做為輸入，並傳回 (可能) 修改過的控制碼。 IFS 提供者必須只將修改過的控制碼提供給其用戶端，而來自用戶端的所有要求只會參考這個修改過的控制碼。 修改過的控制碼在作業系統考慮時，保證與建議的控制碼不區分。 因此，在大部分的情況下，服務提供者只會選擇在所有的內部處理中使用修改過的控制碼。 這項修改函式的目的是要讓 Ws2 \_32.dll 能夠大幅簡化識別與指定之通訊端相關聯之服務提供者的流程。

未傳回 IFS 控制碼的提供者，必須透過 WPUCreateSocketHandle 呼叫從 Ws232.dll 取得有效的控制碼 \_ 。 [](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) NonIFS 提供者必須只提供 Windows 通訊端 2.DLL 提供給其用戶端的控制碼，而來自用戶端的所有要求只會參考這些控制碼。 為了方便服務提供者實施， **WPUCreateSocketHandle** 中提供者所提供的其中一個輸入參數是 DWORD 內容值。 Ws232.dll 會將 \_ 此內容值與配置的通訊端控制碼建立關聯，並允許服務提供者隨時透過 [**WPUQuerySocketHandleCoNtext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) 呼叫來取得內容值。 此內容值的一般用途是將指標儲存至用來儲存通訊端狀態資訊的服務提供者維護的資料結構。

 

 
