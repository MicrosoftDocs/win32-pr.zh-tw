---
description: 設定選擇性回呼函式的指標，此函式會計算已完成的球面調和 (SH) 計算的百分比，並為呼叫端提供中止模擬器的選項。
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine：： SetCallBack 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847357"
---
# <a name="id3dxprtenginesetcallback-method"></a>ID3DXPRTEngine：： SetCallBack 方法

設定選擇性回呼函式的指標，此函式會計算已完成的球面調和 (SH) 計算的百分比，並為呼叫端提供中止模擬器的選項。

## <a name="syntax"></a>語法


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCB* \[在\]
</dt> <dd>

類型： **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)回呼函式的指標，此函式會計算已完成的 SH 計算百分比。 必須實回呼函式，以傳回「 \_ 確定」，以繼續執行模擬器。 任何其他值都會中止模擬器。

</dd> <dt>

*頻率* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

回呼呼叫的頻率。 頻率的反函數大約是回呼函數的呼叫次數。

</dd> <dt>

*lpUserCoNtext* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

傳遞給回呼函式的使用者定義值的指標。 通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值為 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
