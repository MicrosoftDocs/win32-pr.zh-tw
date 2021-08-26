---
description: 為指定的介面建立 (DC) 的裝置內容。
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: 'NtGdiDdGetDC 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 200635ca71ab16a84a137f85be13cc4fdbb6db200e4c0da795d07f945f06e9f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053338"
---
# <a name="ntgdiddgetdc-function"></a>NtGdiDdGetDC 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

為指定的介面建立 (DC) 的裝置內容。

## <a name="syntax"></a>語法


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)或 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)先前傳回之核心模式 DirectDraw 介面的控制碼。

</dd> <dt>

*puColorTable* \[在\]
</dt> <dd>

傳回之 DC 的覆寫色彩表指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回有效的 **HDC**;否則，它會傳回 **Null**。

## <a name="remarks"></a>備註

在任何指定時間，每個介面只允許一個 DC。 **NtGdiDdGetDC** 的後續呼叫將會失敗，直到釋放先前的 DC 為止。

建議應用程式改為呼叫 [IDirectDrawSurface7：： GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) ，以與作業系統無關的方式提供相同的功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Ntgdi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[圖形低層級用戶端支援](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
