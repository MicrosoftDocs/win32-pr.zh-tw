---
title: GetTSAudioEndpointEnumeratorForSession 回呼函式
description: 傳回指定之會話識別碼之音訊端點列舉值的參考。
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- GetTSAudioEndpointEnumeratorForSession 回呼函式遠端桌面服務
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f64af1d7e886b418ac87cd360302101a60d746d707652f605a648e9812a5547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059586"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>GetTSAudioEndpointEnumeratorForSession 回呼函式

傳回指定之會話識別碼之音訊端點列舉值的參考。 此音訊端點列舉值的取用者（例如 MMDevAPI.dll）會呼叫此函式，以在遠端桌面服務會話中取出音訊端點列舉值。

## <a name="syntax"></a>語法


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SessionId* \[在\]
</dt> <dd>

遠端桌面服務會話的識別碼。

</dd> <dt>

*ppEndpointEnumerator* \[擴展\]
</dt> <dd>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**。

## <a name="remarks"></a>備註

標頭檔中未定義此函式。 您應該在自訂端點列舉值中執行並匯出此函式，並使用本主題稍早語法區塊中所示的簽章。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>         |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[執行自訂音訊端點列舉值](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

