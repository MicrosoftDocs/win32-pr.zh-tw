---
description: NtGdiDdCreateSurface 函式-將介面附加至另一個介面。
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: 'NtGdiDdCreateSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085776"
---
# <a name="ntgdiddcreatesurface-function"></a>NtGdiDdCreateSurface 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

將介面附加至另一個介面。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDraw* \[在\]
</dt> <dd>

代表驅動程式之 [**DD \_ DIRECTDRAW \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) 結構的控制碼。

</dd> <dt>

*hSurface* \[在\]
</dt> <dd>

相同介面的先前控制碼。 如果介面是在模式切換之後重新建立，則會使用。

</dd> <dt>

*puSurfaceDescription* \[in、out\]
</dt> <dd>

描述驅動程式應建立之介面或緩衝區的 [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) 結構指標。

</dd> <dt>

*puSurfaceGlobalData* \[in、out\]
</dt> <dd>

[**DD \_ 介面 \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global)結構的指標，其中包含與多個表面全域共用的表面資料。

</dd> <dt>

*puSurfaceLocalData* \[in、out\]
</dt> <dd>

[**DD \_ 介面 \_ 本機**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構清單的指標，描述驅動程式所建立的介面物件。

</dd> <dt>

*puSurfaceMoreData* \[in、out\]
</dt> <dd>

[**DD \_ 介面 \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more)的指標，此結構包含額外的本機介面資料。

</dd> <dt>

*puCreateSurfaceData* \[in、out\]
</dt> <dd>

[**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata)結構的指標，其中包含建立表面所需的資訊。

</dd> <dt>

*puhSurface* \[擴展\]
</dt> <dd>

供 DirectDraw API 使用，而且不應該由驅動程式填入。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdCreateSurface** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt> </dl>    | 驅動程式已執行作業，並傳回該操作的有效傳回碼。 如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。 否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt> </dl> | 驅動程式對要求的作業沒有任何批註。 如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。 否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。<br/> |



 

## <a name="remarks"></a>備註

建議您的應用程式呼叫 [IDirectDraw7：： CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) ，而不是使用此函數。

建立一連串的連接表面（例如交換鏈或鏈或 mipmap）時，應該先針對每個介面呼叫 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) 。 然後呼叫 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) 來附加它們。 最後，只針對鏈中的第一個介面呼叫 **NtGdiDdCreateSurface** 。 在此情況下， *hSurface* 會是 **NtGdiDdCreateSurfaceObject** 針對鏈中第一個介面所傳回的控制碼。

只應呼叫 **NtGdiDdCreateSurface** ，以在本機和非本機視訊記憶體中建立介面。 永遠不應該呼叫它來建立系統記憶體表面。 若要建立系統記憶體表面，請改用 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) 。

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

 

 
