---
description: 取得與媒體金鑰會話相關聯的錯誤狀態。
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: IMFMediaKeySession：： GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7698d059bd7d930037096208668de91292bca9e67b13743d353d3f682ec905a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357758"
---
# <a name="imfmediakeysessiongeterror-method"></a>IMFMediaKeySession：： GetError 方法

取得與媒體金鑰會話相關聯的錯誤狀態。

## <a name="syntax"></a>語法


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*code* 
</dt> <dd>

錯誤碼。

</dd> <dt>

*systemCode* 
</dt> <dd>

平臺特定錯誤資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




