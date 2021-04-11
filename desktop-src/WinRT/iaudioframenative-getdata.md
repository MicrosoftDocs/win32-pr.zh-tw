---
description: 這個方法會傳回提供音訊資料存取權的介面。
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: IAudioFrameNative：：：：的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113121"
---
# <a name="iaudioframenativegetdata-method"></a>IAudioFrameNative：：：：的方法

這個方法會傳回提供音訊資料存取權的介面。

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

類型： **REFIID**

要取出之介面的 IID。

</dd> <dt>

*ppv* \[擴展\]
</dt> <dd>

類型： **LPVOID \** _

當這個方法成功傳回時，會包含 _riid * 參數中要求的介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

\_在成功完成時傳回 S OK。 \_如果找不到要求的介面，則傳回 E NOINTERFACE。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



