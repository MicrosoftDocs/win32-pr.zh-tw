---
description: 當 tablet 內容終結時發生。
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: ITabletEventSink：： CoNtextDestroy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514016"
---
# <a name="itableteventsinkcontextdestroy-method"></a>ITabletEventSink：： CoNtextDestroy 方法

當 tablet 內容終結時發生。

## <a name="syntax"></a>語法


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tcid* \[在\]
</dt> <dd>

要終結的 tablet 內容識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 




