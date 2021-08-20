---
description: 關閉媒體金鑰會話，且必須在金鑰會話發行之前呼叫。
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: IMFMediaKeySession：： Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: f172f88f0e13acd3d44f673e5a142fafe9f7075677d8496b5332af0607e89846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062987"
---
# <a name="imfmediakeysessionclose-method"></a>IMFMediaKeySession：： Close 方法

關閉媒體金鑰會話，且必須在金鑰會話發行之前呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT Close();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




