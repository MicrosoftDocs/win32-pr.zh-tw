---
description: 由 Microsoft DirectDraw 和 Microsoft Direct3D 執行時間使用，可從驅動程式取得其目前狀態的相關資訊。
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: 'NtGdiD3DGetDriverState 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970095"
---
# <a name="ntgdid3dgetdriverstate-function"></a>NtGdiD3DGetDriverState 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 相反地，請使用 DirectDraw 和 Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

由 Microsoft DirectDraw 和 Microsoft Direct3D 執行時間使用，可從驅動程式取得其目前狀態的相關資訊。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[in、out\]
</dt> <dd>

描述驅動程式狀態之 [**DD \_ GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiD3DGetDriverState** 會傳回下列其中一個回呼碼。



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

 

 
