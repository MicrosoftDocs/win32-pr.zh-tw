---
description: GetStreamCaps 方法會取得與指定之格式索引相關聯的功能。
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl：： GetStreamCaps 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f54cbd44a946c0fcd3cf297c4cacadc49369765b8c1b6505031a145768c3b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406108"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>ITFormatControl：： GetStreamCaps 方法

\[此方法無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**GetStreamCaps** 方法會取得與指定之格式索引相關聯的功能。

## <a name="syntax"></a>語法


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

正在探查之格式的索引。

</dd> <dt>

*ppMediaType* \[擴展\]
</dt> <dd>

終端機格式的 **AM \_ 媒體 \_ 類型** 描述元指標。 如需 **\_ 媒體 \_ 類型** 的詳細資訊，請參閱 DirectX 檔。

</dd> <dt>

*pStreamConfigCaps* \[擴展\]
</dt> <dd>

提供有關資料流程功能詳細資訊的 [**TAPI \_ 串流設定 \_ \_ cap**](tapi-stream-config-caps.md) 結構。

</dd> <dt>

*pfEnabled* \[擴展\]
</dt> <dd>

指出是否已啟用與目前索引相關聯的格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**TAPI \_ 串流 \_ 設定 \_ CAP**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




