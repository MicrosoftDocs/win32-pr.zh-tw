---
description: ISCardDatabase 介面提供執行智慧卡資源管理員的資料庫作業的方法。
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: 'ISCardDatabase 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971002"
---
# <a name="iscarddatabase-interface"></a>ISCardDatabase 介面

\[**ISCardDatabase** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardDatabase** 介面提供執行 [*智慧卡*](../secgloss/s-gly.md)[*資源管理員的*](../secgloss/r-gly.md)資料庫作業的方法。 這些作業包括列出已知的智慧卡、 [*讀取*](../secgloss/r-gly.md)器和讀取器群組，以及抓取智慧卡和其 [*主要服務提供者*](../secgloss/p-gly.md)所支援的介面。

> [!Note]  
> 主要服務提供者的識別碼是 COM GUID，可用來具現化和使用特定卡片的 COM 物件。

 

下列範例顯示 **ISCardDatabase** 介面的一般用法。 在此情況下， **ISCardDatabase** 介面會用來列出所有已知的智慧卡。

**將交易提交至特定卡片**

1.  建立 **ISCardDatabase** 介面。
2.  呼叫 [**ListCards**](iscarddatabase-listcards.md) ，以根據 [*ATR 字串*](../secgloss/a-gly.md) 或其支援的介面來取得所有已知的智慧卡。
3.  釋放 **ISCardDatabase** 介面。

## <a name="members"></a>成員

**ISCardDatabase** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardDatabase** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardDatabase** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | 抓取特定智慧卡之 [*主要服務提供者*](../secgloss/p-gly.md) 的識別碼。<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | 抓取特定智慧卡支援的所有介面 (Guid) 的介面識別碼。<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | 抓取符合一組特定介面識別碼 (Guid) 或 [*ATR 字串*](../secgloss/a-gly.md)的所有智慧卡名稱。<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | 抓取資源管理員有知識的 [*讀者群組*](../secgloss/r-gly.md) 名稱。<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | 取得資源管理員有知識的 [*讀者*](../secgloss/r-gly.md) 名稱。<br/>                                          |



 

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
| IID<br/>                      | IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
