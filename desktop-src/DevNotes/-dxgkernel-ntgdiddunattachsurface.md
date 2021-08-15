---
description: 移除在兩個核心模式介面物件之間，以 NtGdiDdAttachSurface 建立的附件。
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: 'NtGdiDdUnattachSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7bc5abd09c9a7372bb693a3220d2f059e393ed2df17af87c1187b9c927fdb627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386868"
---
# <a name="ntgdiddunattachsurface-function"></a>NtGdiDdUnattachSurface 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

移除在兩個核心模式介面物件之間，以 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)建立的附件。

## <a name="syntax"></a>語法


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSurface* \[在\]
</dt> <dd>

以 hSurfaceFrom 參數形式傳遞至 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)的核心模式介面物件。

</dd> <dt>

*hSurfaceAttached* \[在\]
</dt> <dd>

以 hSurfaceTo 參數形式傳遞至 NtGdiDdAttachSurface 的核心模式介面物件[ ](-dxgkernel-ntgdiddattachsurface.md)

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdUnattachSurface** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt> </dl>    | 驅動程式已執行作業，並傳回該操作的有效傳回碼。 如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。 否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt> </dl> | 驅動程式對要求的作業沒有任何批註。 如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。 否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。<br/> |



 

## <a name="remarks"></a>備註

建議應用程式使用 DirectDraw API，以較高層級的方式處理介面附件。

不需要呼叫此函式，因為在呼叫 [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) 時，核心會自動終結所有的附件。

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

 

 




