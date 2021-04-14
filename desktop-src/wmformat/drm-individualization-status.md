---
title: 'DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) '
description: 'DRM 的 \_ 個人化 \_ 狀態列舉類型會定義 drm 個人化的有效狀態。 |DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) '
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386407"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) 

**Drm 的 \_ 個人化 \_ 狀態** 列舉類型會定義 drm [*個人化*](wmformat-glossary.md)的有效狀態。 當應用程式透過呼叫 [**IWMDRMReader：：賦予**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)來啟動「個人化」時，會透過呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法，將「個人化」要求的進度傳達給應用程式。 「個人化」狀態訊息將會使用 \_ [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 列舉類型的 WMT 賦予成員做為 *status* 參數。 在 *pValue* 參數中，會將個人化的狀態傳遞給 **OnStatus** 。

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

指出由於呼叫 [**IWMDRMReader：： CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)而取消的個人化處理常式。

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

[**DRM \_ HTTP \_ 狀態**](drm-http-status.md)
</dt> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





