---
title: 'ID3DX11EffectRasterizerVariable GetBackingStore 方法 (D3dx11effect .h) '
description: 取得包含 rasteriser 狀態之變數的指標。
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- GetBackingStore 方法 Direct3D 11
- GetBackingStore 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，GetBackingStore 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80912da541d5d5386da4e9612216db3ce62904bdb32ba262b5a2d1ae773201cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534684"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>ID3DX11EffectRasterizerVariable：： GetBackingStore 方法

取得包含 rasteriser 狀態之變數的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Index* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Rasteriser 狀態原因陣列中的索引。 如果效果中只有一個 rasteriser 變數，請使用0。

</dd> <dt>

*pRasterizerDesc* 
</dt> <dd>

類型： D3D11 轉譯器 **[ **\_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Rasteriser 狀態原因的指標 (參閱 D3D11 轉譯器 [**\_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。 備份存放區資料可以在必要時用來重新建立變數。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

