---
description: 這個類別是影像載入事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971932"
---
# <a name="image_v1_load-class"></a>映射 \_ V1 \_ 載入類別

這個類別是影像載入事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>成員

**映射 \_ V1 \_ 載入** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**映射 \_ V1 \_ 載入** 類別具有這些屬性。

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

要載入之 DLL 或可執行映射的檔案名和副檔名。

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

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**映射 \_ V1**](image-v1.md)
</dt> </dl>

 

 




