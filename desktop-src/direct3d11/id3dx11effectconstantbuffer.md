---
title: 'ID3DX11EffectConstantBuffer 介面 (D3dx11effect .h) '
description: 常數緩衝區介面會存取常數緩衝區或紋理緩衝區。
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- ID3DX11EffectConstantBuffer 介面 Direct3D 11
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323079"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>ID3DX11EffectConstantBuffer 介面

常數緩衝區介面會存取常數緩衝區或紋理緩衝區。

## <a name="members"></a>成員

**ID3DX11EffectConstantBuffer** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。 **ID3DX11EffectConstantBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectConstantBuffer** 介面具有這些方法。



| 方法                                                                             | 描述                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | 取得常數緩衝區。<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | 取得材質緩衝區。<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | 設定常數緩衝區。<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | 設定材質緩衝區。<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | 還原先前設定的常數緩衝區。<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | 還原先前設定的材質緩衝區。<br/>  |



 

## <a name="remarks"></a>備註

使用常數緩衝區來儲存許多效果常數;根據更新頻率將常數分組到緩衝區。 這可讓您將狀態變更的數目降至最低，以及進行最少的 API 呼叫以變更狀態。 這兩個因素都可提升效能。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





