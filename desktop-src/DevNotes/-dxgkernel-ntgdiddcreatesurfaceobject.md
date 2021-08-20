---
description: 建立核心模式介面物件，此物件表示 puSurfaceLocal 所參考的使用者模式介面物件。
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: 'NtGdiDdCreateSurfaceObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956537"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>NtGdiDdCreateSurfaceObject 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

建立核心模式介面物件，此物件表示 *puSurfaceLocal* 所參考的使用者模式介面物件。

## <a name="syntax"></a>語法


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDrawLocal* \[在\]
</dt> <dd>

核心模式 DirectDraw 物件的控制碼。

</dd> <dt>

*hSurface* \[在\]
</dt> <dd>

相同介面的先前控制碼。 如果介面是在模式切換之後重新建立，則會使用。

</dd> <dt>

*puSurfaceLocal* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的指標，代表要與配置的記憶體相關聯的 DirectDraw 使用者模式介面物件。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*puSurfaceMore* \[在\]
</dt> <dd>

[**DD 介面的指標 \_ \_ 更多**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more)結構，其中包含每個個別介面物件的額外本機資料。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*puSurfaceGlobal* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global)結構的指標，其中包含全域與多個表面共用的介面資料。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*bComplete* \[在\]
</dt> <dd>

核心模式物件完成旗標。 可以是下列其中一個值。

<dt>



  (TRUE) 


</dt> <dd>

完成有關核心模式表示的所有處理。

</dd> <dt>



  (FALSE) 


</dt> <dd>

建立物件，但不設定內部資料，例如記憶體指標。 使用 **FALSE** 建立的物件可以使用 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) 來附加，而且是透過呼叫 [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)來完成。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回核心模式介面標記法的控制碼;否則，它會傳回 **Null**。

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
