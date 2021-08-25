---
description: 設定媒體來源的持續時間（100-毫微秒單位）。
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: IMFMediaSourceExtension：： SetDuration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061208"
---
# <a name="imfmediasourceextensionsetduration-method"></a>IMFMediaSourceExtension：： SetDuration 方法

設定媒體來源的持續時間（100-毫微秒單位）。

## <a name="syntax"></a>語法


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*持續時間* \[在\]
</dt> <dd>

媒體來源的持續時間（100-毫微秒單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




