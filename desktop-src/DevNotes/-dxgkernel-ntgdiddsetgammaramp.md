---
description: 設定裝置的 gamma 斜坡。
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: 'NtGdiDdSetGammaRamp 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 78e68a76fed6db78a2f3d247c5bec1b73f3df3b6fe204e0d09b1bc5f14a014b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668807"
---
# <a name="ntgdiddsetgammaramp-function"></a>NtGdiDdSetGammaRamp 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

設定裝置的 gamma 斜坡。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDraw* \[在\]
</dt> <dd>

要設定其曲線之核心模式驅動程式物件的控制碼。

</dd> <dt>

*hdc* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*lpGammaRamp* \[在\]
</dt> <dd>

**DDGAMMARAMP** 結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **TRUE** 。 否則，它會是 **Null**。

## <a name="remarks"></a>備註

建議應用程式改為使用 **IDirectDrawGammaControl：： SetGammaRamp** 或 [**IDirect3DDevice9：： SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 方法，因為這些方法提供的功能與作業系統無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Ntgdi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[圖形低層級用戶端支援](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
