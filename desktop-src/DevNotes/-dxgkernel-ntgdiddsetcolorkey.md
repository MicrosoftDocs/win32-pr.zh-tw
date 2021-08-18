---
description: 設定指定之介面的色彩索引鍵值。
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: 'NtGdiDdSetColorKey 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a803853c8df50da740ea6930f769334704ffd7dfcd771590cfb3e4fccb9cf9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911950"
---
# <a name="ntgdiddsetcolorkey-function"></a>NtGdiDdSetColorKey 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

設定指定之介面的色彩索引鍵值。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的指標，描述要與色彩索引鍵相關聯的介面。

</dd> <dt>

*puSetColorKeyData* \[in、out\]
</dt> <dd>

[**DD \_ SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata)結構的指標，其中包含為指定介面設定色彩索引鍵所需的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdSetColorKey** 會傳回下列其中一個回呼碼。



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

 

 
