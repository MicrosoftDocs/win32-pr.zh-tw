---
title: 'ICM_GETINFO 訊息 (Vfw .h) '
description: ICM \_ GETINFO 訊息會查詢視訊壓縮驅動程式，以在 ICINFO 結構中傳回本身的描述。
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966120"
---
# <a name="icm_getinfo-message"></a>ICM \_ GETINFO 訊息

**ICM \_ GETINFO** 訊息會查詢視訊壓縮驅動程式，以在 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)結構中傳回本身的描述。


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

要包含資訊之 **ICINFO** 結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

**ICINFO** 的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) 的大小（以位元組為單位），如果發生錯誤則傳回零。

## <a name="remarks"></a>備註

一般而言，應用程式會傳送此訊息，以顯示已安裝的壓縮機清單。

驅動程式應填滿 **szDriver** 以外的 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)結構的所有成員。

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

 

 





