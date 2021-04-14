---
title: IAMWMBufferPass SetNotify 方法
description: 應用程式會使用 SetNotify 方法，以應用程式的 IAMWMBufferPassCallback 介面指標提供 WM ASF 寫入器或 WM ASF 讀取器篩選器。
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- SetNotify 方法 windows Media 格式
- SetNotify 方法 windows Media Format，IAMWMBufferPass 介面
- IAMWMBufferPass 介面 windows Media Format，SetNotify 方法
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382530"
---
# <a name="iamwmbufferpasssetnotify-method"></a>IAMWMBufferPass：： SetNotify 方法

應用程式會使用 **SetNotify** 方法，以應用程式的 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)介面指標提供 wm Asf 寫入器或 [WM asf 讀取](wm-asf-reader-filter.md)器篩選器。

## <a name="syntax"></a>語法


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCallback* \[在\]
</dt> <dd>

應用程式 **IAMWMBufferPassCallback** 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

請先呼叫這個方法，然後再將篩選圖形置於執行狀態。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMWMBufferPass 介面**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 