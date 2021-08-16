---
description: 針對指定的核心模式 Microsoft DirectDraw 介面物件，釋放先前建立的裝置內容 (DC) 。
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: 'NtGdiDdReleaseDC 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: daa4cad2f6f3937ebe29b3996ebbaa72b894ee743f97222cb1f6e2ff61f7dbb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824908"
---
# <a name="ntgdiddreleasedc-function"></a>NtGdiDdReleaseDC 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

針對指定的核心模式 Microsoft DirectDraw 介面物件，釋放先前建立的裝置內容 (DC) 。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

先前建立之核心模式 DirectDraw 介面物件的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

需要取得 DirectDraw 介面之 DC 的應用程式可能會使用 [IDirectDrawSurface7：： GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc)，它會以與作業系統無關的方式來公開這項功能。

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

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
