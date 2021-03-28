---
description: 這個類別是檔案資訊事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973557"
---
# <a name="fileio_info-class"></a>FileIo \_ 資訊類別

這個類別是檔案資訊事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>成員

**FileIo \_ Info** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FileIo \_ Info** 類別具有這些屬性。

<dl> <dt>

**>extrainfo**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，指標
</dt> </dl>

針對 FileDispositionInformation 要求，此欄位包含要求的配置。 針對 FileEndOfFileInformation 和 FileAllocationInformation 要求，此欄位包含指定的檔案大小。

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，指標
</dt> </dl>

若要判斷檔案名，請將這個屬性的值與 [**FileIo \_ name**](fileio-name.md)事件的 **FileObject** 屬性比對。

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，指標
</dt> </dl>

可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

要求的檔案資訊類別。

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

IO 要求封包。 這個屬性會識別 IO 活動。

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

執行作業之執行緒的執行緒識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

設定資訊和查詢資訊事件表示已設定或查詢檔案屬性。 發出 FSCTL 命令時，會記錄檔案系統控制項 (FSControl) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




