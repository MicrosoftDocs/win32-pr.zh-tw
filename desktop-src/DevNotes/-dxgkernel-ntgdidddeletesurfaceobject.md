---
description: NtGdiDdDeleteSurfaceObject 會刪除先前建立的核心模式介面物件。
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: 'NtGdiDdDeleteSurfaceObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972539"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>NtGdiDdDeleteSurfaceObject 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

**NtGdiDdDeleteSurfaceObject** 會刪除先前建立的核心模式介面物件。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

先前建立之核心模式介面物件的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。 這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。

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

[**DdDeleteSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
