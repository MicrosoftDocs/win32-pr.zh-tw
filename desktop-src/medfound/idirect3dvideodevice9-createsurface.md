---
description: 建立適用于 DirectX Video 加速 (DXVA) 解碼的壓縮表面。
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9：： CreateSurface 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115212"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9：： CreateSurface 方法

建立適用于 DirectX Video 加速 (DXVA) 解碼的壓縮表面。

若要取得介面需求，請呼叫 [**IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) ，並檢查傳回的 [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) 結構。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* 
</dt> <dd>

介面的寬度（以圖元為單位）。 將此參數設定為等於 **DXVACompBufferInfo. WidthToCreate**。

</dd> <dt>

*高度* 
</dt> <dd>

介面的高度（以圖元為單位）。 將此參數設定為等於 **DXVACompBufferInfo. HeightToCreate**。

</dd> <dt>

*BackBuffers* 
</dt> <dd>

背景緩衝區的數目。 這個參數可以是零。

</dd> <dt>

*格式* 
</dt> <dd>

像素格式，指定為 **D3DFORMAT** 值。 請將此參數設定為 **DXVACompBufferInfo 格式**。

</dd> <dt>

*集區* 
</dt> <dd>

要在其中建立介面的記憶體集區，指定為 **D3DPOOL** 值。 將此參數設定為等於 **DXVACompBufferInfo**。

</dd> <dt>

*使用量* 
</dt> <dd>

一或多個 **D3DUSAGE** 常數的位 **or** 。 將此參數設定為等於 **DXVACompBufferInfo。**

</dd> <dt>

*ppSurface* 
</dt> <dd>

接收 **IDirect3DSurface9** 介面的指標。 呼叫端必須釋放介面。

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

保留的。 設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




