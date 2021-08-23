---
description: 轉譯基本專案，並傳回更新後的呈現狀態。
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: 'NtGdiD3DDrawPrimitives2 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8d3964a9946da37d211aab0e5949cff5e09a40dcc18607aabb3a0c13c37acfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833658"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

轉譯基本專案，並傳回更新後的呈現狀態。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCmdBuf* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，識別包含命令資料的 DirectDraw 介面。

</dd> <dt>

*hVBuf* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，識別包含頂點資料的 DirectDraw 介面。

</dd> <dt>

*pded* \[in、out\]
</dt> <dd>

[**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/)結構的指標，其中包含驅動程式呈現一或多個基本專案所需的資訊。

</dd> <dt>

*pfpVidMemCmd* \[in、out\]
</dt> <dd>

如果驅動程式交換命令緩衝區，則為視訊記憶體的新指標。

</dd> <dt>

*pdwSizeCmd* \[in、out\]
</dt> <dd>

指定驅動程式必須增加交換命令緩衝區的最小位元組數目。

</dd> <dt>

*pfpVidMemVtx* \[in、out\]
</dt> <dd>

如果驅動程式交換了頂點緩衝區，則為視訊記憶體的新指標。

</dd> <dt>

*pdwSizeVtx* \[in、out\]
</dt> <dd>

指定驅動程式必須為交換頂點緩衝區配置的最小位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiD3DDrawPrimitives2** 會傳回下列其中一個回呼碼。



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

 

 
