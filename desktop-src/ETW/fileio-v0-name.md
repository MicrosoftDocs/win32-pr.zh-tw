---
description: FileIo \_ V0 \_ Name 類別是檔案 i/o 事件之事件種類類別的較舊版本。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694259"
---
# <a name="fileio_v0_name-class"></a>FileIo \_ V0 \_ Name 類別

**FileIo \_ V0 \_ Name** 類別是檔案 i/o 事件之事件種類類別的較舊版本。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>成員

**FileIo \_ V0 \_ Name** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FileIo \_ V0 \_ Name** 類別具有這些屬性。

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

檔案的完整路徑，不包括磁碟機號。

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

將 this 指標的值符合 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)事件中的 **FileObject** 指標值，以判斷 i/o 作業的類型。

</dd> </dl>

## <a name="remarks"></a>備註

**Windows Server 2003：** 若要取得檔案名路徑的磁碟機號，請使用 **FileObject** 屬性值對應至對應的 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) 事件。 從 **DiskIo \_ TypeGroup1** 事件中，使用 **DiskNumber** 和 **ByteOffset** 屬性值對應至對應的 [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) 事件。 **DriveLetterString** 屬性包含磁碟機號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> </dl>

 

 




