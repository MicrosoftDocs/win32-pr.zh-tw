---
title: 'ISoftKbd Initialize 方法 (Softkbdc .h) '
description: ISoftKbd Initialize 方法會初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialize 方法文字服務架構
- Initialize 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，Initialize 方法
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685584"
---
# <a name="isoftkbdinitialize-method"></a>ISoftKbd：： Initialize 方法

**ISoftKbd：： Initialize** 方法會初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                | 描述                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法成功。<br/> |



 

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
</dt> </dl>

 

 





