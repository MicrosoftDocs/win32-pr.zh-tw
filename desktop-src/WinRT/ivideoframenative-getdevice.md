---
description: 這個方法會傳回與影片資料相關聯的裝置。
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: IVideoFrameNative：： GetDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386153"
---
# <a name="ivideoframenativegetdevice-method"></a>IVideoFrameNative：： GetDevice 方法

這個方法會傳回與影片資料相關聯的裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

要取出之裝置的 IID。

</dd> <dt>

*ppv* \[擴展\]
</dt> <dd>

當此方法成功傳回時，會包含在 *riid* 參數中要求的裝置指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_在成功完成時傳回 S OK。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



