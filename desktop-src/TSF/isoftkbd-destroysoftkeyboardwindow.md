---
title: 'ISoftKbd DestroySoftKeyboardWindow 方法 (Softkbdc .h) '
description: ISoftKbd DestroySoftKeyboardWindow 方法會終結軟鍵盤視窗。
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- DestroySoftKeyboardWindow 方法文字服務架構
- DestroySoftKeyboardWindow 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，DestroySoftKeyboardWindow 方法
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966116"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>ISoftKbd：:D estroySoftKeyboardWindow 方法

**ISoftKbd：:D estroysoftkeyboardwindow** 方法會終結軟鍵盤視窗。

## <a name="syntax"></a>語法


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                | 描述                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會移除先前使用 [**ISoftKbd：： CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)的呼叫所建立的軟鍵盤視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





