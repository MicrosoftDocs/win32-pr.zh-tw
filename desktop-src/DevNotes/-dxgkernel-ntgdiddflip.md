---
description: 導致與目標和目前表面相關聯的介面記憶體被交換。
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: 'NtGdiDdFlip 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847280"
---
# <a name="ntgdiddflip-function"></a>NtGdiDdFlip 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

導致與目標和目前表面相關聯的介面記憶體被交換。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurfaceCurrent* \[在\]
</dt> <dd>

描述目前介面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼。

</dd> <dt>

*hSurfaceTarget* \[在\]
</dt> <dd>

描述目標介面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼，也就是驅動程式應該翻轉的介面。

</dd> <dt>

*hSurfaceCurrentLeft* \[在\]
</dt> <dd>

描述目前左表面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼。

</dd> <dt>

*hSurfaceTargetLeft* \[在\]
</dt> <dd>

[DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx)結構的控制碼，描述要翻轉至的左側目標介面。

</dd> <dt>

*puFlipData* \[in、out\]
</dt> <dd>

[DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx)結構的指標，其中包含執行 flip 所需的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdFlip** 會傳回下列其中一個回呼碼。



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

 

 




