---
description: 在模式切換之後，重新啟用 Microsoft DirectDraw 核心模式裝置物件。
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: 'NtGdiDdReenableDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 808e2e74492b9a3e828e09389e04f0e1e4b09fef9a63fdd7a22d81521b3df30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045568"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>NtGdiDdReenableDirectDrawObject 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

在模式切換之後，重新啟用 Microsoft DirectDraw 核心模式裝置物件。

## <a name="syntax"></a>語法


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDirectDrawLocal* \[在\]
</dt> <dd>

需要重新啟用的 DirectDraw 物件。

</dd> <dt>

*pubNewMode* \[in、out\]
</dt> <dd>

BOOL 的指標，將會填入表示顯示模式是否已變更的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功 (可以重新啟用裝置) ，此函式會傳回 **TRUE**。 否則 (例如，顯示驅動程式已變更) ，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

重新啟用物件之後，就可以透過呼叫 [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md)來重新查詢裝置的功能。

建議應用程式使用 DirectDraw 或 [Direct3D](../direct3d10/d3d10-graphics-reference.md) 8 版的 api，以與作業系統無關的方式將此程式自動化及抽象化。

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

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
