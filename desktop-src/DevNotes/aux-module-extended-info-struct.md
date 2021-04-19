---
description: 包含擴充的模組資訊。
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: 'AUX_MODULE_EXTENDED_INFO 結構 (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981389"
---
# <a name="aux_module_extended_info-structure"></a>AUX \_ 模組 \_ 擴充 \_ 資訊結構

包含擴充的模組資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**BasicInfo**
</dt> <dd>

[**AUX \_ 模組 \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md)結構。

</dd> <dt>

**ImageSize**
</dt> <dd>

已載入模組的大小（以位元組為單位）。

</dd> <dt>

**FileNameOffset**
</dt> <dd>

**FullPathName** 緩衝區內檔案名的位移。

</dd> <dt>

**FullPathName**
</dt> <dd>

模組的完整路徑。

</dd> </dl>

## <a name="remarks"></a>備註

您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows 輔助 API 程式庫1.0 版或更新版本<br/>                          |
| 標頭<br/>          | <dl> <dt>Aux \_ klib。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**AUX \_ 模組 \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




