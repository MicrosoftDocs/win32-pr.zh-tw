---
description: 建立內容。
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: 'NtGdiD3DCoNtextCreate 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: a11ae1d1e9b9469f22971ec3fc7447d8552b6d263bb43f4a8fe336ccbbc37a69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017736"
---
# <a name="ntgdid3dcontextcreate-function"></a>NtGdiD3DCoNtextCreate 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

建立內容。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDrawLocal* \[在\]
</dt> <dd>

核心模式 DirectDraw 物件的控制碼，先前以 [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)建立，代表要建立 Direct3D 內容的裝置。

</dd> <dt>

*hSurfColor* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，描述要當做轉譯目標使用的 DirectDraw 介面。

</dd> <dt>

*hSurfZ* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，描述要當做深度緩衝區使用的 DirectDraw 介面。 如果這個成員是 **Null**，則不會執行深度緩衝。

</dd> <dt>

*pdcci* \[in、out\]
</dt> <dd>

[**D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/)結構的指標，其中包含建立內容所需的資訊，以及驅動程式應儲存在新內容中的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiD3DCoNtextCreate** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
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

 

 
