---
title: 'D2D1_TAG (D2d1) '
description: 應用程式定義的64位值，用於 \ 160; 標記一組轉譯作業。
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317207"
---
# <a name="d2d1_tag"></a>D2D1 \_ 標記

用來標記一組轉譯作業的應用程式定義64位值。


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>備註

若要在一連串轉譯作業之前設定標記，請使用 [**ID2D1RenderTarget：： SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 方法。 若要取出目前的標記，請使用 [**ID2D1RenderTarget：： GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1。h</dt> </dl>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

