---
title: IDWriteTextLayout3 InvalidateLayout 方法
description: 使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。 如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- InvalidateLayout 方法直接寫入
- InvalidateLayout 方法 Direct Write，IDWriteTextLayout3 介面
- IDWriteTextLayout3 介面 Direct Write，InvalidateLayout 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816079"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>IDWriteTextLayout3：： InvalidateLayout 方法

使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。 如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。

## <a name="syntax"></a>語法


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                 |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





