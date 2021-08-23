---
description: 提供建立和管理智慧卡應用程式協定資料單位 (APDU) 所需的方法。
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: 'ISCardCmd 介面 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e6bce160cfb326f0c44b2fca1c6676b895d9eeeec434826d7fc595fc178c47d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008137"
---
# <a name="iscardcmd-interface"></a>ISCardCmd 介面

\[**ISCardCmd** 介面可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardCmd** 介面提供了建立和管理 [*智慧卡*](../secgloss/s-gly.md)[*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 所需的方法。 此介面會封裝兩個緩衝區：

-   APDU 緩衝區包含將傳送到卡片的命令順序。
-   APDUReply 緩衝區包含執行 APDU 命令之後從卡片傳回的資料 (此資料也稱為「傳回的 APDU」) 。

下列範例顯示 **ISCardCmd** 介面的一般用法。 **ISCardCmd** 介面是用來建立 APDU。

**將交易提交至特定卡片**

1.  建立 [**ISCard**](iscard.md) 介面並連接至智慧卡。
2.  建立 **ISCardCmd** 介面。
3.  使用 [**ISCardISO7816**](iscardiso7816.md) 介面或 **ISCardCmd** 的其中一個組建方法，建立智慧卡 APDU 命令。
4.  藉由呼叫適當的 [**ISCard**](iscard.md) 介面方法，在智慧卡上執行命令。
5.  評估傳回的回應。
6.  視需要重複此程式。
7.  視需要釋放 **ISCardCmd** 介面和其他專案。

## <a name="members"></a>成員

**ISCardCmd** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardCmd** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ISCardCmd** 介面具有這些方法。



| 方法                                       | 描述                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | 為傳輸到智慧卡的有效命令 APDU 進行結構化。<br/>                               |
| [**清除**](iscardcmd-clear.md)             | 清除 APDU 和回復 APDU 訊息緩衝區。<br/>                                             |
| [**封裝**](iscardcmd-encapsulate.md) | 將指定的命令 APDU 封裝到另一個命令 APDU，以傳輸至智慧卡。<br/> |



 

### <a name="properties"></a>屬性

**ISCardCmd** 介面具有這些屬性。



| 屬性                                                              | 存取類型           | 描述                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | 讀取/寫入<br/> | 目前的替代類別識別碼值。<br/>                                                                                                                        |
| [**Apdu**](iscardcmd-get-apdu.md)<br/>                         | 讀取/寫入<br/> | 原始 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 。<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | 唯讀<br/>  | APDU 的長度。<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | 讀取/寫入<br/> | [*回復 APDU*](../secgloss/r-gly.md)。<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | 讀取/寫入<br/> | 回復 APDU 的長度。<br/>                                                                                                                                |
| [**ClassId**](iscardcmd-get-classid.md)<br/>                   | 讀取/寫入<br/> | APDU 的類別識別碼。<br/>                                                                                                                                    |
| [**資料**](iscardcmd-get-data.md)<br/>                         | 唯讀<br/>  | APDU 的資料欄位。<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | 讀取/寫入<br/> | 來自 APDU 的指令識別碼位元組。<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | 唯讀<br/>  | APDU 的 Le 欄位。<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | 讀取/寫入<br/> | 節點位址。<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | 讀取/寫入<br/> | APDU 的第一個參數位元組。<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | 讀取/寫入<br/> | APDU 的第二個參數位元組。<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | 唯讀<br/>  | APDU 的第三個參數位元組。<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | 讀取/寫入<br/> | 信用卡在回復訊息中使用的節點位址。<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | 讀取/寫入<br/> | [*回復 APDU*](../secgloss/r-gly.md) 訊息狀態字組。<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | 唯讀<br/>  | 回復 APDU 的 message SW1 status byte。<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | 唯讀<br/>  | 回復 APDU 的 message SW2 status byte。<br/>                                                                                                                    |
| **類型**<br/>                                                   | 唯讀<br/>  | 保留供未來使用。<br/>                                                                                                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
