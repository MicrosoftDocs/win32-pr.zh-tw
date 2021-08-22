---
title: 'ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView 方法 (D3dx11effect .h) '
description: 取得未排序的存取權。
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- GetUnorderedAccessView 方法 Direct3D 11
- GetUnorderedAccessView 方法 Direct3D 11，ID3DX11EffectUnorderedAccessViewVariable 介面
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，GetUnorderedAccessView 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ccb890d7f03a2066cb7e01633f057e821e34c74521e1bba37f9694ba72a194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676778"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a>ID3DX11EffectUnorderedAccessViewVariable：： GetUnorderedAccessView 方法

取得未排序的存取權。

## <a name="syntax"></a>語法


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppResource* 
</dt> <dd>

類型： **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)指標的指標，該指標會在傳回時設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





