---
title: 'ID3DX11Effect Optimize 方法 (D3dx11effect) '
description: 將效果所需的記憶體數量降到最低。
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- 優化方法 Direct3D 11
- 優化方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，Optimize 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992331"
---
# <a name="id3dx11effectoptimize-method"></a>ID3DX11Effect：： Optimize 方法

將效果所需的記憶體數量降到最低。

## <a name="syntax"></a>語法


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

效果會使用兩種不同方式的記憶體空間：儲存執行時間執行效果所需的資訊，以及儲存使用 API 將資訊反映回應用程式所需的中繼資料。 您可以藉由呼叫 **ID3DX11Effect：： Optimize** 來將反映中繼資料從記憶體中移除，以將效果所需的記憶體數量降到最低。 移除反映資料之後，用來讀取變數的 API 方法將無法再運作。

在效果上呼叫 Optimize 之後，下列方法將會失敗。

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect：： GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> 在呼叫 **ID3DX11Effect：** ： optimize 之前，使用這些方法抓取的參考在呼叫 **ID3DX11Effect：： optimize** 之後仍有效。 這可讓應用程式取得所有將使用的變數、技術和傳遞、呼叫 Optimize，然後使用效果。

 

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





