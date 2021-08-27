---
description: 附加兩個核心模式介面表示。
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: 'NtGdiDdAttachSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088028"
---
# <a name="ntgdiddattachsurface-function"></a>NtGdiDdAttachSurface 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

附加兩個核心模式介面表示。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurfaceFrom* \[在\]
</dt> <dd>

核心模式介面物件的控制碼，該物件將會成為新附件的起點。

</dd> <dt>

*hSurfaceTo* \[在\]
</dt> <dd>

核心模式介面物件的控制碼，該物件將會成為新附件的結束點。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdAttachSurface** 會傳回下列其中一項：



| 傳回碼                                                                          | 描述                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 函式呼叫成功。<br/> |
| <dl> <dt>**假**</dt> </dl> | 函式呼叫失敗。<br/>    |



 

## <a name="remarks"></a>備註

請參閱 DirectDraw 軟體發展工具組 (SDK) 和驅動程式開發工具組 (DDK) 以取得 surface 附件的完整描述。

> [!Note]  
> 如同其他介面附件，所產生的附件是單向的。 呼叫此函式之後， *hSurfaceTo* 將不會附加至 *hSurfaceFrom*。

 

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

 

 




