---
description: 提供支援其他智慧卡 COM 介面的使用者所需的方法。
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: 'ISCardTypeConv 介面 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849251"
---
# <a name="iscardtypeconv-interface"></a>ISCardTypeConv 介面

\[**ISCardTypeConv** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ISCardTypeConv** 介面提供支援其他 [*智慧卡*](../secgloss/s-gly.md)COM 介面的使用者所需的方法。 這個介面僅提供回溯相容性，不應再使用。

## <a name="members"></a>成員

**ISCardTypeConv** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardTypeConv** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardTypeConv** 介面具有這些方法。



| 方法                                                                              | 描述                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | 將典型的 C/c + + 位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | 將對應至通用位元組緩衝區的位元組陣列 (**IStream** 物件) 轉換為一般 C/c + + 位元組陣列。<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | 將對應至位元組 (**IStream** 物件) 的位元組陣列轉換成不帶正負號 char (byte) 的 SAFEARRAY。<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | 將定義為 SAFEARRAY 的位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | 建立位元組陣列。<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | 建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件的通用位元組緩衝區。<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | 建立不帶正負號字元的自動化 SAFEARRAY， (位元組) 。<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | 釋放由 **IStream** COM 介面管理之 HGLOBAL 記憶體區塊的記憶體指標。<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | 取得由 **IStream** COM 介面管理的 HGLOBAL 記憶體區塊的位元組指標。<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | 決定 **IStream** COM 介面)  (位元組數的大小。<br/>                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
