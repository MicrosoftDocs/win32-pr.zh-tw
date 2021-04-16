---
description: 可讓您開啟及管理智慧卡的連接。
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: 'ISCard 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512761"
---
# <a name="iscard-interface"></a>ISCard 介面

\[**ISCard** 介面可用於 [需求] 區段中指定的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCard** 介面可讓您開啟及管理 [*智慧卡*](../secgloss/s-gly.md)的連接。 每張卡片的連接都需要單一的對應 **ISCard** 介面實例。

每次建立 **ISCard** 的實例時，都必須可以使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)。 如果此服務無法使用，則建立介面將會失敗。

下列範例顯示 **ISCard** 介面的一般用法。 **ISCard** 介面是用來連接智慧卡、提交 [*交易*](../secgloss/t-gly.md)，以及釋出智慧卡。

**將交易提交至特定卡片**

1.  建立 **ISCard** 介面。
2.  藉由指定智慧卡 [*讀卡機*](../secgloss/r-gly.md) 或使用先前建立的有效控制碼，連接到智慧卡。
3.  使用 [**ISCardCmd**](iscardcmd.md)建立交易命令，並 [**ISCardISO7816**](iscardiso7816.md) 智慧卡介面。
4.  使用 **ISCard** 提交交易命令以供智慧卡處理。
5.  使用 **ISCard** 釋放智慧卡。
6.  釋放 **ISCard** 介面。

## <a name="members"></a>成員

**ISCard** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCard** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ISCard** 介面具有這些方法。



| 方法                                          | 描述                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | 將物件附加至開啟和設定的智慧卡控點。<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | 在指定的讀取器中開啟智慧卡。<br/>                                                                                                                                                                            |
| [**中斷連結**](iscard-detach.md)                 | 關閉智慧卡的開啟連接。<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | 宣告智慧卡的獨佔存取權。<br/>                                                                                                                                                                           |
| [**附加**](iscard-reattach.md)             | 重設並重新初始化智慧卡。<br/>                                                                                                                                                                             |
| [**交易**](iscard-transaction.md)       |  ([*應用程式協定資料單位*](../secgloss/a-gly.md)) 物件，執行智慧卡命令的寫入和讀取作業。<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | 釋放智慧卡的獨佔存取權。<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>屬性

**ISCard** 介面具有這些屬性。



| 屬性                                               | 存取類型          | Description                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | 唯讀<br/> | 抓取智慧卡的 [*ATR 字串*](../secgloss/a-gly.md) 。<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | 唯讀<br/> | 抓取連接智慧卡的控制碼。<br/>                                                                                                                                  |
| [**Context**](iscard-get-context.md)<br/>       | 唯讀<br/> | 抓取目前的 [*resource manager 內容*](../secgloss/r-gly.md) 控制碼。<br/>                            |
| [**通訊協定**](iscard-get-protocol.md)<br/>     | 唯讀<br/> | 抓取智慧卡上目前正在使用的通訊協定識別碼。<br/>                                                                                                        |
| [**狀態**](iscard-get-status.md)<br/>         | 唯讀<br/> | 抓取 [*智慧卡*](../secgloss/s-gly.md)所在的目前 [*狀態*](../secgloss/s-gly.md)。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
