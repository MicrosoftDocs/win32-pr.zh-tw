---
description: 用來指出來源緩衝區發生錯誤。
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: IMFSourceBufferNotify：： OnError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996617"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>IMFSourceBufferNotify：： OnError 方法

用來指出來源緩衝區發生錯誤。

## <a name="syntax"></a>語法


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hr* \[在\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




