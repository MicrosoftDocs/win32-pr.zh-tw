---
title: 'WM_INDIVIDUALIZE_STATUS 結構 (Drmexternals .h) '
description: WM \_ 賦予 \_ 狀態結構會記錄個人化處理常式的狀態。
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991310"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS 結構 (Drmexternals .h) 

**WM \_ 賦予 \_ 狀態** 結構會記錄 [*個人化*](wmformat-glossary.md)處理常式的狀態。

## <a name="syntax"></a>語法


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**小時**
</dt> <dd>

**HRESULT** 傳回碼。

</dd> <dt>

**enIndiStatus**
</dt> <dd>

[**DRM 的 \_ 個人化 \_ 狀態**](drm-individualization-status.md)列舉類型的值。

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

以 null 結束的字串指標，其中包含了「個人化回應 URL」。

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** ，指出已完成的個人化服務的 HTTP 往返次數。

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

[**DRM \_ HTTP \_ 狀態**](drm-http-status.md)列舉類型的值。

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** ，包含到現在為止下載的位元組數目。

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** ，包含要下載的總位元組數。 您可以使用此值和 **dwHTTPReadProgress** 來顯示使用者介面，指出已完成的下載數量，以及剩餘的時間。

</dd> </dl>

## <a name="remarks"></a>備註

當事件等於 WMT 賦予時，DRM 執行時間元件會填入此結構，並將其傳送至應用程式 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)方法的 *pValue* 參數中的應用程式 \_ 。 應用程式會在下載過程中多次收到此事件。

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

[**結構**](structures.md)
</dt> </dl>

 

 





