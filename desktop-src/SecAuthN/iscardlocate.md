---
description: ISCardLocate 介面提供用來依名稱尋找智慧卡的服務。
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: 'ISCardLocate 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70679a2decc62011df70e68c119365bb8a98f7bdb06af6d7989eac18e7c14fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922927"
---
# <a name="iscardlocate-interface"></a>ISCardLocate 介面

\[**ISCardLocate** 介面可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardLocate** 介面提供用來依名稱尋找 [*智慧卡*](../secgloss/s-gly.md)的服務。

此介面可以顯示智慧卡 [*使用者介面*](../secgloss/u-gly.md) （如有需要）。

下列案例顯示 **ISCardLocate** 介面的一般用法。 **ISCardLocate** 介面可用來建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 。

**使用名稱找出特定的卡片**

1.  建立 **ISCardLocate** 介面。
2.  呼叫 [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) 以搜尋智慧卡名稱。
3.  呼叫 [**FindCard**](iscardlocate-findcard.md) 以搜尋智慧卡。
4.  解譯解譯。
5.  釋放 **ISCardLocate** 介面。

## <a name="members"></a>成員

**ISCardLocate** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardLocate** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardLocate** 介面具有這些方法。



| 方法                                                                  | 描述                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | 保留供未來使用。<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | 指定要在搜尋中使用的卡片名稱。<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | 搜尋智慧卡，並對其開啟有效的連接。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
