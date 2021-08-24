---
description: WPD \_ 位元速率 \_ 類型列舉類型會描述音訊檔案壓縮類型。
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: 'WPD_BITRATE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704048"
---
# <a name="wpd_bitrate_types-enumeration"></a>WPD \_ 位元速率 \_ 類型列舉

**WPD \_ 位元速率 \_ 類型** 列舉類型會描述音訊檔案的壓縮類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_未使用 WPD 位元速率 \_ 類型 \_**
</dt> <dd>

未指定這個值。

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD \_ 位元速率 \_ 類型 \_ 離散**
</dt> <dd>

固定位元速率壓縮。

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD \_ 位元速率 \_ 類型 \_ 變數**
</dt> <dd>

變數位元速率壓縮。

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD \_ 位元速率 \_ 類型 \_ 免費**
</dt> <dd>

自由格式位速度。 這是比允許的最大位元速率低的固定位元速率。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




