---
title: 'WM_INDIVIDUALIZE_STATUS 結構 (Wmdrmsdk .h) '
description: WM \_ 賦予 \_ 狀態結構會保存有關暫止的個人化程式的資訊。
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997763"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS 結構 (Wmdrmsdk .h) 

**WM \_ 賦予 \_ 狀態** 結構會保存有關暫止的個人化程式的資訊。

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

[**DRM [ \_ \_ 狀態**](drmdrm-individualization-status.md)] 列舉類型中的值，指出目前的個人化處理狀態。

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

以 null 結束的字串指標，其中包含了「個人化回應 URL」。

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

已完成的個人化服務的 HTTP 往返次數。

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

[**DRM \_ HTTP \_ 狀態**](drmdrm-http-status.md)列舉類型的值。

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

已下載的位元組數目。

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

要下載的總位元組數。 您可以使用此值和 **dwHTTPReadProgress** 來顯示使用者介面，指出已完成的下載數量，以及剩餘的時間。

</dd> </dl>

## <a name="remarks"></a>備註

當您呼叫 [**IWMDRMIndividualizationStatus：： GetStatus**](iwmdrmindividualizationstatus-getstatus.md) 方法時，就會收到此結構。 它包含呼叫時暫止的個人化處理常式的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





