---
description: 這個類別是 file create 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972204"
---
# <a name="fileio_create-class"></a>FileIo \_ Create 類別

這個類別是 file create 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a>成員

**FileIo \_ Create** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FileIo \_ Create** 類別具有這些屬性。

<dl> <dt>

**CreateOptions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

傳遞至 *CreateOptions* 和 *CreateDispositions* 參數的值會傳遞給 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) 函數。

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

傳遞至 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)函數的 *FileAttributes* 參數值。

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

**OpenPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

檔案的路徑。

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

傳遞至 [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)函數的 *ShareAccess* 參數值。

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

建立檔案之執行緒的執行緒識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 
