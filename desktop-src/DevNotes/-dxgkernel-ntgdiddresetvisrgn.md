---
description: 用來啟用使用者模式，以對桌上型電腦上 windows 的裁剪區域有效瞭解。 這項裁剪可能會從使用者模式執行緒的觀點來非同步變更。
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: 'NtGdiDdResetVisrgn 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3077351b804f854520cff421fcad8a575278bb5a960f60ef760db38e7ca2f3a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833638"
---
# <a name="ntgdiddresetvisrgn-function"></a>NtGdiDdResetVisrgn 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

用來啟用使用者模式，以對桌上型電腦上 windows 的裁剪區域有效瞭解。 這項裁剪可能會從使用者模式執行緒的觀點來非同步變更。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

屬於 DirectDraw 裝置之任何介面的使用者模式物件的指標，其為要重設剪切的物件。 如需詳細資訊，請參閱 DDK 檔。

</dd> <dt>

*hwnd* \[在\]
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

從使用者模式執行緒的觀點來看，裁剪可能會以非同步方式變更。 DirectDraw 和 Windows 圖形裝置介面的核心模式部分 (GDI) 維護計數器，此計數器會在整個桌面的剪切清單變更時遞增。 呼叫此函式會將此計數器記錄到系統上的每個現有 DirectDraw 主要介面。

當 IDirectDrawSurface7：： Blt 或 IDirectDrawSurface7：： Lock 作業修改其中一個主要表面時， [：：](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) 或 [：： Lock](/previous-versions/ms858221(v=msdn.10)) 作業會進行修改， (查看 DDK 檔) ，則會將與此介面一起錄製的計數器與全域計數器進行比較。 如果這些值不同，則會將錯誤碼 DDERR \_ VISRGNCHANGED 傳回給使用者模式程式碼。 然後，使用者模式程式碼將會重新查詢桌面目前的剪輯、呼叫 **NtGdiDdResetVisrgn**，然後重新嘗試套用至主要表面的 IDirectDrawSurface7：： Blt，並採用新的裁剪。 最後，使用者模式程式碼所取樣的裁剪將會與核心模式所擁有的目前裁剪相同，而且會允許 IDirectDrawSurface7：： Blt 繼續進行。

建議應用程式使用 [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) 介面或 [IDirect3DDevice8：:P](/previous-versions/ms889707(v=msdn.10)) 重新傳送的方法來處理非同步裁剪變更。 這些結構會以自動化與作業系統無關的方式來執行非同步裁剪。

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

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
