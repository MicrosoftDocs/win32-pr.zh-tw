---
description: 傳回核心模式 Microsoft DirectX API 控制碼，以用於對控制 DirectX API 機制之核心模式進入點的後續呼叫中使用。
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: 'NtGdiDdGetDxHandle 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973384"
---
# <a name="ntgdiddgetdxhandle-function"></a>NtGdiDdGetDxHandle 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

傳回核心模式 Microsoft DirectX API 控制碼，以用於對控制 DirectX API 機制之核心模式進入點的後續呼叫中使用。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDraw* \[在\]
</dt> <dd>

擁有介面之 DirectDraw 物件的控制碼。 這個參數是選擇性的，可以設定為 **Null**。

</dd> <dt>

*hSurface* \[在\]
</dt> <dd>

要傳回核心模式 DirectX API 控制碼的介面。 這個參數是選擇性的，可以設定為 **Null**。

</dd> <dt>

*bRelease* \[在\]
</dt> <dd>

如果應該釋放 DirectX API 核心模式介面，則設定為 **TRUE** 。 否則 **為 FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

用於後續 DirectX API 導向核心進入點的 DirectX API 控制碼。

## <a name="remarks"></a>備註

如果同時指定 *hDirectDraw* 和 *hSurface* ，則會忽略 *hSurface* 。

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

 

 




