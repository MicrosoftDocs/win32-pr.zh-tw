---
description: 應用程式會執行此方法。 呼叫 ID3DXAnimationController：： AdvanceTime 期間，在其中一個追蹤中設定動畫的回呼時，會呼叫這個方法。
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler：： HandleCallback 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12fcfa0feba1d239cf72c37e78fec63140dda4f954e7c48dffd643dcca4400c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279208"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>ID3DXAnimationCallbackHandler：： HandleCallback 方法

應用程式會執行此方法。 呼叫 [**ID3DXAnimationController：： AdvanceTime**](id3dxanimationcontroller--advancetime.md)期間，在其中一個追蹤中設定動畫的回呼時，會呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

回呼發生所在之追蹤的識別碼。

</dd> <dt>

*pCallbackData* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

使用者擁有的回呼資料指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法的傳回值是由應用程式設計人員所執行。 一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。 否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
