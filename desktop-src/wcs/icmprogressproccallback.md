---
title: ICMProgressProcCallback 回呼函式
description: ICMProgressProcCallback 函式是由應用程式提供的回呼函式，它會報告進度，並允許應用程式取消色彩處理。
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- ICMProgressProcCallback 回呼函式 Windows 色彩系統
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d697bb09b4871f6debb1a41a7ecc3e795307ee544ec30bfaf4b5b44ba0328578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671384"
---
# <a name="icmprogressproccallback-callback-function"></a>ICMProgressProcCallback 回呼函式

**ICMProgressProcCallback** 函式是由應用程式提供的回呼函式，它會報告進度，並允許應用程式取消色彩處理。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulMax* 
</dt> <dd>

指定進度計數器的最大值 (用來預估點陣圖處理) 的完成。

</dd> <dt>

*ulCurrent* 
</dt> <dd>

指定進度計數器的目前值除以最大值時 (，提供完成) 百分比的粗略估計。

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

指定應用程式傳遞至 ICM2 函式的資料，然後將其傳遞至回呼函數。 例如，您可以使用這類資料來識別要報告進度的點陣圖和處理常式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回 **TRUE** 以繼續點陣圖處理。 傳回值為 **FALSE** ，表示取消處理。 如果取消處理，呼叫的函式會傳回零以表示失敗，雖然可能會部分填滿其輸出緩衝區。

## <a name="remarks"></a>備註

這個回呼函式的名稱是由應用程式所提供。 許多 WCS 函式（包括 [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) 和 [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)）會定期呼叫此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Icm。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[函數](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
