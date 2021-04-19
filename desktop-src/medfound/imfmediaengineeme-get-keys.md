---
description: 取得與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體索引鍵物件，則為 null。
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: IMFMediaEngineEME：： get_Keys 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982149"
---
# <a name="imfmediaengineemeget_keys-method"></a>IMFMediaEngineEME：： get \_ Keys 方法

取得與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體索引鍵物件，則 **為 null** 。

## <a name="syntax"></a>語法


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*鑰匙* 
</dt> <dd>

與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體按鍵物件則為 **null** 。

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

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




