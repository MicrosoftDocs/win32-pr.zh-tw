---
description: IByteBuffer 介面是提供來讀取、寫入和管理資料流程物件。 此物件基本上是 IStream 物件的包裝函式。
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: 'IByteBuffer 介面 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945038"
---
# <a name="ibytebuffer-interface"></a>IByteBuffer 介面

\[**IByteBuffer** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]

**IByteBuffer** 介面是提供來讀取、寫入和管理資料流程物件。 此物件基本上是 **IStream** 物件的包裝函式。

## <a name="members"></a>成員

**IByteBuffer** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IByteBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IByteBuffer** 介面具有這些方法。



| 方法                                           | 描述                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**克隆**](ibytebuffer-clone.md)               | 複製 **IByteBuffer** 物件。<br/>                                                              |
| [**Commit**](ibytebuffer-commit.md)             | 認可 [*交易*](/windows/desktop/SecGloss/t-gly)。<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | 將位元組複製到另一個物件。<br/>                                                                |
| [**初始化**](ibytebuffer-initialize.md)     | 初始化 **IByteBuffer** 物件。<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | 限制存取範圍的位元組。<br/>                                                          |
| [**讀**](ibytebuffer-read.md)                 | 將位元組讀入記憶體。<br/>                                                                       |
| [**恢復**](ibytebuffer-revert.md)             | 捨棄上次 [**認可**](ibytebuffer-commit.md) 呼叫之後的變更。<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | 變更 seek 指標。<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | 變更資料流物件的大小。<br/>                                                         |
| [**統計**](ibytebuffer-stat.md)                 | 捕獲資料流程的統計資訊。<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | 移除 [**LockRegion**](ibytebuffer-lockregion.md)先前設定的存取限制。<br/>     |
| [**寫**](ibytebuffer-write.md)               | 將位元組寫入資料流程。<br/>                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardssp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

