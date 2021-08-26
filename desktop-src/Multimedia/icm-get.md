---
title: 'ICM_GET 訊息 (Vfw .h) '
description: ICM \_ GET 訊息會從視訊壓縮驅動程式抓取應用程式定義的 DWORD 值。
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038728"
---
# <a name="icm_get-message"></a>ICM \_取得訊息

**ICM \_ GET** 訊息會從視訊壓縮驅動程式抓取應用程式定義的 **DWORD** 值。


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*光伏*
</dt> <dd>

要以目前狀態填滿之記憶體區塊的指標。 您也可以指定 **Null** 來判斷狀態資訊所需的記憶體數量。

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回儲存狀態資訊所需的記憶體數量（以位元組為單位）。

## <a name="remarks"></a>備註

用來代表狀態資訊的結構是驅動程式特定的，而且是由驅動程式所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 





