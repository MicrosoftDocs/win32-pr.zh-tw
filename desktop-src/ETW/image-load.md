---
description: 這個類別是影像事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Image_Load 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513096"
---
# <a name="image_load-class"></a>映射 \_ 載入類別

這個類別是影像事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>成員

**映射 \_ 載入** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**映射 \_ 載入** 類別具有這些屬性。

<dl> <dt>

DefaultBase
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) ，指標
</dt> </dl>

預設基底位址。

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (12) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

DLL 或可執行檔映射的檔案名和副檔名。

</dd> <dt>

Imagebase 設定
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，指標
</dt> </dl>

載入映射之應用程式的基底位址。

</dd> <dt>

ImageCheckSum
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

影像檢查總和。

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，指標
</dt> </dl>

所載入映射的大小。

使用這個屬性時，這個屬性的資料類型實際上是大小 \_ t。 指標辨識符號用來判斷大小 \_ t 是4個位元組或8個位元組。

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

識別載入影像的進程。

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

保留的。

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

保留的。

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) 
</dt> </dl>

保留的。

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) 
</dt> </dl>

保留的。

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (11) 
</dt> </dl>

保留的。

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

載入或卸載映射的時間和日期。

</dd> </dl>

## <a name="remarks"></a>備註

DCStart 和 DCEnd 事件會分別列舉追蹤開頭和結尾的所有載入的影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Image**](image.md)
</dt> <dt>

[**影像 \_ V0**](image-v0.md)
</dt> <dt>

[**映射 \_ V1**](image-v1.md)
</dt> </dl>

 

 




