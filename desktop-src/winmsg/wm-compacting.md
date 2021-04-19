---
description: 當系統偵測到超過30到60秒間隔的系統時間超過12.5% 時，就會傳送至所有最上層視窗，以壓縮記憶體。 這表示系統記憶體不足。
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: 'WM_COMPACTING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975788"
---
# <a name="wm_compacting-message"></a>WM \_ 壓縮訊息

當系統偵測到超過30到60秒間隔的系統時間超過12.5% 時，就會傳送至所有最上層視窗，以壓縮記憶體。 這表示系統記憶體不足。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> [!Note]  
> 此訊息僅提供給以16位 Windows 為基礎的應用程式相容。

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

中央處理單位 (CPU) 時間的比率，目前由系統壓縮記憶體到系統執行其他作業所花費的 CPU 時間。 例如，0x8000 代表花費在壓縮記憶體的 CPU 時間50%。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

當應用程式收到此訊息時，應該盡可能釋放最多的記憶體，將應用程式目前的活動層級以及系統上執行的應用程式總數納入考慮。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows 總覽](windows.md)
</dt> </dl>

 

 
