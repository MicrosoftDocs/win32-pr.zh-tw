---
description: 使用指定的初始化資料和自訂資料，建立媒體金鑰會話物件。 .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: IMFMediaKeys：： CreateSession 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2dd9bcc7a1151b042d275917e8bd8106eb079de3315137ca41fa7faecaf5c957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942038"
---
# <a name="imfmediakeyscreatesession-method"></a>IMFMediaKeys：： CreateSession 方法

使用指定的初始化資料和自訂資料，建立媒體金鑰會話物件。 .

## <a name="syntax"></a>語法


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mimeType* 
</dt> <dd>

用於內容之媒體容器的 MIME 類型。

</dd> <dt>

*initData* 
</dt> <dd>

金鑰系統的初始化資料。

</dd> <dt>

*Cb* 
</dt> <dd>

*InitData* 的計數（以位元組為單位）。

</dd> <dt>

*customData* 
</dt> <dd>

傳送至金鑰系統的自訂資料。

</dd> <dt>

*cbCustomData* 
</dt> <dd>

*CbCustomData* 的計數（以位元組為單位）。

</dd> <dt>

*通知* 
</dt> <dd>

通知

</dd> <dt>

*ppSession* 
</dt> <dd>

媒體金鑰會話。

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

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




