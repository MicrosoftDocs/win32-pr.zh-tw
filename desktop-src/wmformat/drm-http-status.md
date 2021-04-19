---
title: 'DRM_HTTP_STATUS 列舉 (Drmexternals .h) '
description: DRM \_ HTTP \_ 狀態列舉類型會定義 drm 要求的狀態範圍。
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968978"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>DRM_HTTP_STATUS 列舉 (Drmexternals .h) 

**Drm \_ HTTP \_ 狀態** 列舉類型會定義 [*drm*](wmformat-glossary.md)要求的狀態範圍。

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**
</dt> <dd>

尚未起始 HTTP 作業。

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP \_ 連接**
</dt> <dd>

正在建立連接。

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP \_ 要求**
</dt> <dd>

正在要求資料。

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP \_ 接收**
</dt> <dd>

正在接收資料。

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ 已完成**
</dt> <dd>

HTTP 作業已完成。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md) 結構所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                      |
| 版本<br/>                  | Windows Media Format 7 SDK 或更新版本的 SDK<br/>                       |
| 標頭<br/>                   | <dl> <dt>Drmexternals。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 的 \_ 個人化 \_ 狀態**](drm-individualization-status.md)
</dt> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





