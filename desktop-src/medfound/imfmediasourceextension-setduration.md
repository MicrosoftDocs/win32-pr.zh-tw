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
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974766"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




