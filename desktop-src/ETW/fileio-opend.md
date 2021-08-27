---
description: 這個類別是檔案操作結束事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: 74042df74f8e128c4d92b6e4f1c886a7bba2f673c1a8a998a4b7f251475c3f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130588"
---
# <a name="fileio_opend-class"></a>FileIo \_ OpEnd 類別

這個類別是檔案操作結束事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>成員

**FileIo \_ OpEnd** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FileIo \_ OpEnd** 類別具有這些屬性。

<dl> <dt>

**>extrainfo**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

檔案系統針對作業所傳回的額外資訊。 例如，讀取要求是所讀取的實際位元組數目。

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

IO 要求封包。 這個屬性會識別正在結束的 IO 活動。

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

從作業傳回值。

</dd> </dl>

## <a name="remarks"></a>備註

[**FileIo**](fileio.md) 事件會在作業開始時記錄。 OpEnd 事件可以個別啟用，以指出這些作業的結尾。 Irp 可以用來將開始和結束事件相互關聯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




