---
description: 開始處理以建立解碼的圖片。
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9：： BeginFrame 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974235"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>IDirect3DDXVADevice9：： BeginFrame 方法

開始處理以建立解碼的圖片。

## <a name="syntax"></a>語法


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDstSurface* 
</dt> <dd>

未壓縮目的介面之 **IDirect3DSurface9** 介面的指標。

</dd> <dt>

*SizeInputData* 
</dt> <dd>

*PInputData* 所指定的緩衝區大小（以位元組為單位）。 值必須是2。

</dd> <dt>

*pInputData* 
</dt> <dd>

包含影片加速器資料之緩衝區的指標。 這個緩衝區必須包含以零為基底的框架索引，並指定為 **文字** 值。

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

*POutputData* 所指定的緩衝區大小（以位元組為單位）。 此值必須為零。

</dd> <dt>

*pOutputData* 
</dt> <dd>

影片加速器可以寫入之緩衝區的指標。 將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

對於 **BeginFrame** 的每個呼叫，解碼器都必須對 [**IDirect3DDXVADevice9：： EndFrame**](idirect3ddxvadevice9-endframe.md)進行對應的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




