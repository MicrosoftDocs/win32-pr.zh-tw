---
title: 'ICM_CONFIGURE 訊息 (Vfw .h) '
description: ICM \_ 設定訊息會通知視訊壓縮驅動程式顯示其設定對話方塊，或查詢視訊壓縮驅動程式來判斷它是否有設定對話方塊。
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d9176415c22a1b79a8dc08ee84db1c77fbd6665f89f615b38d3c60538d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784998"
---
# <a name="icm_configure-message"></a>ICM \_設定訊息

**ICM \_ 設定** 訊息會通知視訊壓縮驅動程式顯示其設定對話方塊，或查詢視訊壓縮驅動程式來判斷它是否有設定對話方塊。 您可以使用 [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) 宏明確地傳送此訊息。


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*hwnd*
</dt> <dd>

顯示之對話方塊的父視窗控制碼。 您可以在此參數中指定1，以判斷驅動程式是否有設定對話方塊，如同在 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) 宏中一樣。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。

## <a name="remarks"></a>備註

此訊息不同于用於硬體設定的 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息。 此訊息的對話方塊應可讓使用者設定和編輯 [**ICM \_ >getstate**](icm-getstate.md)所參考的內部狀態，並 [**ICM \_ SETSTATE**](icm-setstate.md)訊息。 例如，此對話方塊可讓使用者變更影響品質層級和其他類似壓縮選項的參數。

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

 

 





