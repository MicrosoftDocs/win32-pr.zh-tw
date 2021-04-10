---
title: 'ICM_GETSTATE 訊息 (Vfw .h) '
description: ICM \_ >getstate 訊息會查詢視訊壓縮驅動程式，以在記憶體區塊中傳回其目前的設定，或判斷取出設定資訊所需的記憶體數量。
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106548"
---
# <a name="icm_getstate-message"></a>ICM \_ >getstate 訊息

**ICM \_ >getstate** 訊息會查詢視訊壓縮驅動程式，以在記憶體區塊中傳回其目前的設定，或判斷取出設定資訊所需的記憶體數量。 您可以使用 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) 宏明確地傳送此訊息。


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*光伏*
</dt> <dd>

包含目前設定資訊之記憶體區塊的指標。 您可以為此參數指定 **Null** ，以判斷設定資訊所需的記憶體數量，如 [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)中所示。

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *pv* 為 **Null**，則會傳回設定資訊所需的記憶體數量（以位元組為單位）。

如果 *pv* 不是 **Null**，則會 \_ 在成功時傳回 ICERR OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

用來表示設定資訊的結構是驅動程式特定的，而且是由驅動程式所定義。

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

 

 





