---
description: 藉由指定包含巨大區塊的表面、巨大區塊存在的每個介面中的位移，以及要轉譯之巨大區塊資料的大小，告知驅動程式要轉譯的巨大區塊。
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: 'NtGdiDdRenderMoComp 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d057ba1c7b533d75ce10754670b911ddc01a689acee29d79614a3ce2f273d278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827969"
---
# <a name="ntgdiddrendermocomp-function"></a>NtGdiDdRenderMoComp 函式

\[這項功能可能會隨著每個作業系統修訂而變更。 請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]

藉由指定包含巨大區塊的表面、巨大區塊存在的每個介面中的位移，以及要轉譯之巨大區塊資料的大小，告知驅動程式要轉譯的巨大區塊。

## <a name="syntax"></a>語法


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMoComp* \[在\]
</dt> <dd>

[**DD \_ MOTIONCOMP \_ 本機**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local)結構的控制碼，其中包含所要求之動作補償的描述。

</dd> <dt>

*puRenderMoCompData* \[in、out\]
</dt> <dd>

[**DD \_ RENDERMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata)結構的指標，其中包含呈現框架所需的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

**NtGdiDdRenderMoComp** 會傳回下列其中一個回呼碼。



| 傳回碼                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt> </dl>    | 驅動程式已執行作業，並傳回該操作的有效傳回碼。 如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。 否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt> </dl> | 驅動程式對要求的作業沒有任何批註。 如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。 否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。<br/> |



 

## <a name="remarks"></a>備註

如需詳細資訊，請參閱 Microsoft (DDK) 的 Microsoft DirectX 影片加速驅動程式開發工具組。

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

 

 
