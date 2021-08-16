---
description: 查詢先前為其功能建立的 Microsoft DirectDraw 物件之核心模式標記法。
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: 'NtGdiDdQueryDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103818"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>NtGdiDdQueryDirectDrawObject 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

查詢先前為其功能建立的 Microsoft DirectDraw 物件之核心模式標記法。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDrawLocal* \[在\]
</dt> <dd>

先前建立之核心模式 DirectDraw 裝置的控制碼。

</dd> <dt>

*pHalInfo* \[擴展\]
</dt> <dd>

將填入裝置功能之 [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) 結構的指標。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

呼叫端提供之緩衝區的指標，此緩衝區會儲存驅動程式回報的回呼旗標。 緩衝區的大小應為3個 \* sizeof (DWORD) ，並以下列順序儲存回呼旗標： pCallBackFlags \[ 0 \] 用於 [**dd \_ 回呼**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks)中的旗標，pCallBackFlags 1 用於 dd SURFACECALLBACKS 中的旗標， \[ \] 而 pCallBackFlags [**\_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks) \[ 2 \] 用於 [**dd \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks)中的旗標。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*puD3dCallbacks* \[擴展\]
</dt> <dd>

Direct3D 回呼指標的資料表指標。 資料表會填入 Gdi32.dll 內模仿 Direct3D 顯示驅動程式的函式指標。 此回呼資料表與 \_ DDK 檔中所討論的 D3DHAL D3DCALLBACKS 結構相同。

</dd> <dt>

*puD3dDriverData* \[擴展\]
</dt> <dd>

[**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata)資料的指標，如 DDK 檔中所述。

</dd> <dt>

*puD3dBufferCallbacks* \[擴展\]
</dt> <dd>

回呼指標資料表的指標。 資料表會填入 Gdi32.dll 內模仿 Direct3D 顯示驅動程式的函式指標。 此回呼資料表與 DDHAL \_ DDEXEBUFCALLBACKS 結構相同，它會對應至 DDK 檔中所討論的 [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) 結構，不同之處在于 **DD \_ D3DBUFCALLBACKS** 中 XxxD3DBuffer 的成員會取代為 XxxExecuteBuffer DDHAL 中的 DDEXEBUFCALLBACKS \_ 。

</dd> <dt>

*puD3dTextureFormats* \[擴展\]
</dt> <dd>

[**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85))結構陣列的指標，定義一組允許的材質格式。

</dd> <dt>

*puNumHeaps* \[擴展\]
</dt> <dd>

[**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)的 **dwNumHeaps** 成員指標。**vmiData**。 **DwNumHeaps** 成員會指定 *puvmList* 中的記憶體堆積數目。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*puvmList* \[擴展\]
</dt> <dd>

影片記憶體堆積描述項清單的指標。 可以是 **Null**。 未使用此參數，因為影片記憶體管理完全是在核心模式中處理。

</dd> <dt>

*puNumFourCC* \[擴展\]
</dt> <dd>

[**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)的 **puNumFourCCCodes** 成員指標。**ddCaps**。 **PuNumFourCCCodes** 成員會指定驅動程式支援的 [四個字元碼 (FOURCC)](../directshow/fourcc-codes.md)碼數目。 請參閱 DDK 檔以取得詳細資料。

</dd> <dt>

*puFourCC* \[擴展\]
</dt> <dd>

支援的 [四個字元代碼清單的指標 (FOURCC) ](../directshow/fourcc-codes.md) 介面格式。 可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

這個函式的呼叫是設計成在兩個步驟的進程中進行。 在第一個步驟中， *puFourCC*、 *puvmList* 和 *puD3dTextureFormats* 應該是 **Null**，而 [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) 會填入 [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)。**ddCaps**。**dwNumFourCCCodes**、 **DD \_ HALINFO**。**vmiData**。**dwNumHeaps** 和 [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata)。**dwNumTextureFormats** ，其中包含要傳回的專案數。 在第二個呼叫中，呼叫端應配置指定大小的陣列，並傳遞這些指標，而不是 *puFourCC*、 *puvmList* 和 *puD3dTextureFormats* 參數中的 **Null** 值。 陣列接著會填入適當的資料。

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

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
