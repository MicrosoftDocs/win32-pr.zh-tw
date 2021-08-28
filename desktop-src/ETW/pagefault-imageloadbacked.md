---
description: 這個類別是分頁檔案事件中映射載入的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75104fcf923ed59bfcc99e214e66a235549b7059ca0e36c41b6f90d308a3efff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811768"
---
# <a name="pagefault_imageloadbacked-class"></a>PageFault \_ ImageLoadBacked 類別

這個類別是分頁檔案事件中映射載入的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>成員

**PageFault \_ ImageLoadBacked** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**PageFault \_ ImageLoadBacked** 類別具有這些屬性。

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，格式 ( "x" ) 
</dt> </dl>

保留的。

</dd> <dt>

**FileChar**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，格式 ( "x" ) 
</dt> </dl>

保留的。

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷檔案的名稱。

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，格式 ( "x" ) 
</dt> </dl>

保留的。

</dd> </dl>

## <a name="remarks"></a>備註

此事件會在建立映射區段期間記錄 (例如，當記憶體管理員判斷映射需要複製到分頁檔案中並從中執行時，DLL 載入) 。 一般而言，映射是從原始程式檔執行，但是當記憶體管理員判斷來源檔案可由現有的寫入器以非同步方式修改，或是當來源檔案位於卸載式媒體或遠端裝置上時，就可能會發生分頁檔案支援。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




