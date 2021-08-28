---
description: 建立 Microsoft DirectDraw 物件的核心端標記法。
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: 'NtGdiDdCreateDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6925932a6a400565ad942abbf845db591a9cb39dcad2559f1e3e8cb3951e51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956687"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>NtGdiDdCreateDirectDrawObject 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

建立 Microsoft DirectDraw 物件的核心端標記法。

## <a name="syntax"></a>語法


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* \[在\]
</dt> <dd>

應建立 DirectDraw 物件的任何 DC 顯示裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此函式會傳回核心模式物件表示的控制碼;否則，它會傳回 **Null**。

## <a name="remarks"></a>備註

建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。 這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。

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

[**DdCreateDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
