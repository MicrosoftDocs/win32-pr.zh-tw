---
description: 終結先前配置的核心模式 Microsoft DirectDraw 介面物件。
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: 'NtGdiDdDestroySurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025915"
---
# <a name="ntgdidddestroysurface-function"></a>NtGdiDdDestroySurface 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

終結先前配置的核心模式 Microsoft DirectDraw 介面物件。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

先前配置之核心模式介面物件的控制碼。

</dd> <dt>

*bRealDestroy* \[在\]
</dt> <dd>

指定如何終結表面。 可以是下列其中一個值。

<dt>



  (TRUE) 


</dt> <dd>

終結表面和可用的視訊記憶體。

</dd> <dt>



  (FALSE) 


</dt> <dd>

釋放視訊記憶體，但讓表面保持未初始化的狀態。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdDestroySurface** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt> </dl>    | 驅動程式已執行作業，並傳回該操作的有效傳回碼。 如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。 否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt> </dl> | 驅動程式對要求的作業沒有任何批註。 如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。 否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。<br/> |



 

## <a name="remarks"></a>備註

建議應用程式使用 DirectDraw 和 Direct3D Api 來建立和終結介面，而不是此函數。

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

 

 




