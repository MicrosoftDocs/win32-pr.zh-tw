---
description: 設定覆迭的位置。
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: 'NtGdiDdSetOverlayPosition 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f4d6b6c11fb2af1aba4b32bb512a5c881239e16ab407f39bbcb82a90dbee7830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386908"
---
# <a name="ntgdiddsetoverlayposition-function"></a>NtGdiDdSetOverlayPosition 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

設定覆迭的位置。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurfaceSource* \[在\]
</dt> <dd>

代表 DirectDraw 重迭表面之 [**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) 結構的控制碼。

</dd> <dt>

*hSurfaceDestination* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的指標，表示正在重迭的介面。

</dd> <dt>

*puSetOverlayPositionData* \[in、out\]
</dt> <dd>

[**DD \_ SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata)結構的指標，其中包含設定重迭位置所需的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdSetOverlayPosition** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt> </dl>    | 驅動程式已執行作業，並傳回該操作的有效傳回碼。 如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。 否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt> </dl> | 驅動程式對要求的作業沒有任何批註。 如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。 否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。<br/> |



 

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

 

 
