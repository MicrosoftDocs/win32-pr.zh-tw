---
description: 這個方法會傳回提供影片資料存取權的介面。
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: IVideoFrameNative：：：：的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993768"
---
# <a name="ivideoframenativegetdata-method"></a>IVideoFrameNative：：：：的方法

這個方法會傳回提供影片資料存取權的介面。

## <a name="syntax"></a>語法


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

要取出之介面的 IID。

</dd> <dt>

*ppv* \[擴展\]
</dt> <dd>

當這個方法成功傳回時，會包含在 *riid* 參數中要求的介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_在成功完成時傳回 S OK。 \_如果找不到要求的介面，則傳回 E NOINTERFACE。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



