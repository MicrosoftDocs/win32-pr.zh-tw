---
description: 啟動使用中的技術。
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect：： Begin 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196291"
---
# <a name="id3dxeffectbegin-method"></a>ID3DXEffect：： Begin 方法

啟動使用中的技術。

## <a name="syntax"></a>語法


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPasses* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

傳回值的指標，指出轉譯目前技術所需的傳遞數目。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD，可決定是否儲存並還原由效果修改的狀態。 預設值0指定 **ID3DXEffect：： Begin** 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 會儲存並還原效果所修改的所有狀態 (包括圖元和頂點著色器常數) 。 有效的旗標可在有效的 [狀態儲存和還原旗標](d3dxfx.md)中看到。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

應用程式會藉由呼叫 **ID3DXEffect：： Begin**，在效果系統中設定一個有效的技術。 效果系統會藉由捕捉狀態欄塊中的技術可變更的所有管線狀態來進行回應。 應用程式會藉由呼叫 [**ID3DXEffect：： end**](id3dxeffect--end.md)（使用狀態欄塊來還原原始狀態）來發出技術的結尾。 因此，效果系統會在技術變成作用中時，負責儲存狀態，並在技術結束時還原狀態。 如果您選擇停用此儲存和還原功能，請參閱 [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md)。

在 **ID3DXEffect：： Begin** 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 配對中，應用程式會使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 來設定使用中的 pass、 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) （如果啟動成功後發生任何狀態變更），並使用 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md) 結束主動傳遞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
