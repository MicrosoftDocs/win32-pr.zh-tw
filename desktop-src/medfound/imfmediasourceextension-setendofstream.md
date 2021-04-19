---
description: 指出已到達媒體資料流程的結尾。
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: IMFMediaSourceExtension：： SetEndOfStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982143"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>IMFMediaSourceExtension：： SetEndOfStream 方法

指出已到達媒體資料流程的結尾。

## <a name="syntax"></a>語法


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[在\]
</dt> <dd>

用來傳遞錯誤資訊。

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
</dt> <dt>

[**MF \_ MSE \_ 錯誤**](mf-mse-error.md)
</dt> </dl>

 

 




