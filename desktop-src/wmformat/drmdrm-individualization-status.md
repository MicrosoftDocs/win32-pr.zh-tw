---
title: 'DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) '
description: 'DRM 的 \_ 個人化 \_ 狀態列舉類型會定義 drm 個人化的有效狀態。 |DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) '
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999677"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) 

**Drm 的 \_ 個人化 \_ 狀態** 列舉類型會定義 drm 個人化的有效狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**\_未定義 INDI**
</dt> <dd>

這個值已保留供未來使用

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ 開始**
</dt> <dd>

表示個人化流程的開始。

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ 成功**
</dt> <dd>

表示已完成的個人化程式。

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI \_ 失敗**
</dt> <dd>

表示無法進行的個人化處理。

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ 取消**
</dt> <dd>

表示應用程式已取消了「個人化」進程。

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI \_ 下載**
</dt> <dd>

指出正在下載安全性升級。

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI \_ 安裝**
</dt> <dd>

指出正在安裝安全性升級。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md) 結構所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](drm-enumeration-types.md)
</dt> </dl>

 

 





