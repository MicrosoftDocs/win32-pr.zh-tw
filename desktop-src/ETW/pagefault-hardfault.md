---
description: 這個類別是硬分頁錯誤事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdabfab80eadc75fa05ffe148363a85cb5ddefad9abb626cfa4e1c3fa6fe2a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394611"
---
# <a name="pagefault_hardfault-class"></a>PageFault \_ HardFault 類別

這個類別是硬分頁錯誤事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a>成員

**PageFault \_ HardFault** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**PageFault \_ HardFault** 類別具有這些屬性。

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

從 ReadOffset 讀取來滿足錯誤的資料量。

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，指標
</dt> </dl>

將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷檔案的名稱。

</dd> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，副檔名 ( "WmiTime" ) 
</dt> </dl>

發生分頁錯誤的開始時間戳。

</dd> <dt>

**ReadOffset**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

從中讀取資料以滿足錯誤的檔案位移。

</dd> <dt>

**TThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，格式 ( "x" ) 
</dt> </dl>

發生分頁錯誤之執行緒的執行緒識別碼。

</dd> <dt>

**VirtualAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，指標
</dt> </dl>

錯誤的位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




