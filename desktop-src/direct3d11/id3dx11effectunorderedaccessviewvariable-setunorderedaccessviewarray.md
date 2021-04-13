---
title: 'ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray 方法 (D3dx11effect .h) '
description: 設定未排序存取-views 的陣列。
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- SetUnorderedAccessViewArray 方法 Direct3D 11
- SetUnorderedAccessViewArray 方法 Direct3D 11，ID3DX11EffectUnorderedAccessViewVariable 介面
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，SetUnorderedAccessViewArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992158"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a>ID3DX11EffectUnorderedAccessViewVariable：： SetUnorderedAccessViewArray 方法

設定未排序存取-views 的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppResources* 
</dt> <dd>

類型： **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)指標的陣列。

</dd> <dt>

*Offset* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

第一個未排序存取視圖的索引。

</dd> <dt>

*Count* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

陣列中的元素數目。

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

 

