---
description: 包含基本的模組資訊。
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: 'AUX_MODULE_BASIC_INFO 結構 (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956147"
---
# <a name="aux_module_basic_info-structure"></a>AUX \_ 模組 \_ 基本 \_ 資訊結構

包含基本的模組資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**Imagebase 設定**
</dt> <dd>

核心位址空間內模組的基底位址。

</dd> </dl>

## <a name="remarks"></a>備註

您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows輔助 API 程式庫1.0 版或更新版本<br/>                          |
| 標頭<br/>          | <dl> <dt>Aux \_ klib。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




