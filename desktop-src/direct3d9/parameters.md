---
description: 參數為效果變數。
ms.assetid: vs|directx_sdk|~\parameters.htm
title: " (Direct3D 9) 的參數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109889"
---
# <a name="parameters-direct3d-9"></a> (Direct3D 9) 的參數

參數為效果變數。

## <a name="syntax"></a>Syntax

*使用類型識別碼* \[ ：*語義* \] \[ < *注釋 (s)* > \] \[ =  *運算式* \] ;

您可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)，從應用程式讀取和寫入參數。

您可以在函式和技術中參考參數， (特別是在) 狀態指派的右側。



| 項目                                                                                 | 描述                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*使用*<br/>                   | 參數的範圍。 請參閱 [ (Direct3D 9) 的使用方式和常 ](usages-and-literals.md)值。<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*類型*<br/>                      | HLSL 型別的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) 。<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*Id*<br/>                            | 唯一名稱。<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*語義*<br/>          | 識別碼規則後面的標記，通常表示參數的使用方式。 必須是特定類型。<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*注釋*<br/> | 零個或更多的使用者專屬資訊。 可以是任何類型。 請參閱 [使用批註將資訊新增至效果參數](using-an-effect.md)。<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*表達*<br/>    | 初始化參數的值。 請參閱 [ (Direct3D 9) 的運算式 ](expressions.md)。<br/>                                                                  |



 

參數可以初始化為 HLSL 運算式的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) ，以縮減為常值。

執行狀態指派或函式呼叫時，不會變更參數值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
