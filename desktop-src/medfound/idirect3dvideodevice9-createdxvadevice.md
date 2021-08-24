---
description: 建立 (DXVA) 解碼器裝置的 DirectX Video 加速。
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9：： CreateDXVADevice 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555728"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>IDirect3DVideoDevice9：： CreateDXVADevice 方法

建立 (DXVA) 解碼器裝置的 DirectX Video 加速。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGuid* 
</dt> <dd>

指定要建立之裝置的 GUID 指標。

</dd> <dt>

*pUncompData* 
</dt> <dd>

[**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)結構的指標，指定未壓縮影像的格式。

</dd> <dt>

*.Pdata* 
</dt> <dd>

**DXVA \_ ConnectMode** 結構的指標，此結構會指定 DXVA 模式和受限的設定檔。

</dd> <dt>

*DataSize* 
</dt> <dd>

**DXVA \_ ConnectMode** 結構的大小（以位元組為單位）。

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

接收 [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) 介面的指標。 呼叫端必須釋放介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




