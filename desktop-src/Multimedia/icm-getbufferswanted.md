---
title: 'ICM_GETBUFFERSWANTED 訊息 (Vfw .h) '
description: ICM 的 \_ GETBUFFERSWANTED 訊息會查詢驅動程式，以取得要配置的緩衝區數目。 您可以使用 ICGetBuffersWanted 宏明確地傳送此訊息。
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495868"
---
# <a name="icm_getbufferswanted-message"></a>ICM \_GETBUFFERSWANTED 訊息

**ICM 的 \_ GETBUFFERSWANTED** 訊息會查詢驅動程式，以取得要配置的緩衝區數目。 您可以使用 [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) 宏明確地傳送此訊息。


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

包含驅動程式所需的樣本數目，以有效率地轉譯資料的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功或 ICERR 不支援，則會傳回 ICERR OK \_ 。

## <a name="remarks"></a>備註

使用硬體轉譯資料的驅動程式會使用這個訊息，並想要確保等待緩衝區抵達時所造成的時間延遲降到一。 例如，如果驅動程式控制的影片解壓縮面板可以容納10個畫面格，則會傳回此訊息的10。 這會指示應用程式在目前需要的畫面格之前，嘗試保留10個框架。

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

 

 





