---
title: 'GetDimensions (DirectX HLSL 材質物件) '
description: 取得材質大小資訊。 語法區塊會顯示在方法宣告中可能的所有參數。 [備註] 區段中的表格會顯示針對每個材質物件類型所執行的參數。
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119834"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (DirectX HLSL 材質物件) 

取得材質大小資訊。 語法區塊會顯示在方法宣告中可能的所有參數。 [備註] 區段中的表格會顯示針對每個材質物件類型所執行的參數。

void Object. GetDimensions ( UINT MipLevel、typeX Width、typeX Height、typeX Elements、typeX Depth、typeX NumberOfLevels、typeX NumberOfSamples ) ;



 

typeX 表示有兩種可能的類型： **uint** 或 **float**。

## <a name="parameters"></a>參數



| 項目                                                                                                                               | 描述                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*<br/>                                     | 除 **緩衝區** 物件以外的任何 [材質物件](dx-graphics-hlsl-to-type.md)類型。<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[以 \] 零為基底的索引，用來識別 mipmap 層級。 如果未使用這個引數，則會假設為第一個 mip 層級。<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*寬度*<br/>                                         | \[輸出 \] 材質寬度，以材質。<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*高度*<br/>                                     | \[\]材質中的材質高度。<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*元素*<br/>                             | \[\]陣列中的元素數目。<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*深度*<br/>                                         | \[\]材質中的材質深度。<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[\]mipmap 層級的數目。<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[\]樣本數。<br/>                                                                                            |



 

## <a name="return-value"></a>傳回值

無

## <a name="overloaded-methods"></a>多載方法

下表列出所有不同版本的方法;版本與輸入參數的數目不同。 請注意，對於採用整數參數的每個方法，有一個使用浮點參數的多載方法。



| Texture-Object 類型 | 輸入參數                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel、UINT Width、UINT NumberOfLevels                                 |
| Texture1D           | UINT 寬度                                                                     |
| Texture1D           | UINT MipLevel、float Width、float NumberOfLevels                               |
| Texture1D           | 浮點數寬度                                                                    |
| Texture1DArray      | UINT MipLevel、UINT Width、UINT 元素、UINT NumberOfLevels                  |
| Texture1DArray      | UINT 寬度、UINT 元素                                                      |
| Texture1DArray      | UINT MipLevel、float Width、float Elements、float NumberOfLevels               |
| Texture1DArray      | 浮點數寬度、浮點數元素                                                    |
| Texture2D           | UINT MipLevel、UINT Width、UINT Height、UINT NumberOfLevels                    |
| Texture2D           | UINT 寬度、UINT 高度                                                        |
| Texture2D           | UINT MipLevel、float Width、float Height、float NumberOfLevels                 |
| Texture2D           | 浮點數寬度、浮點數高度                                                      |
| Texture2DArray      | UINT MipLevel、UINT Width、UINT Height、UINT 元素、UINT NumberOfLevels     |
| Texture2DArray      | UINT Width、UINT Height、UINT 元素                                         |
| Texture2DArray      | UINT MipLevel、float Width、float Height、float Elements、float NumberOfLevels |
| Texture2DArray      | 浮點數寬度、浮點數高度、浮點數元素                                      |
| Texture3D           | UINT MipLevel、UINT Width、UINT Height、UINT Depth、UINT NumberOfLevels        |
| Texture3D           | UINT 寬度、UINT 高度、UINT 深度                                            |
| Texture3D           | UINT MipLevel、float Width、float Height、float Depth、float NumberOfLevels    |
| Texture3D           | 浮點數寬度、浮點數高度、浮點數深度                                         |
| TextureCube         | UINT MipLevel、UINT Width、UINT Height、UINT NumberOfLevels                    |
| TextureCube         | UINT 寬度、UINT 高度                                                        |
| TextureCube         | UINT MipLevel、float Width、float Height、UINT NumberOfLevels                  |
| TextureCube         | 浮點數寬度、浮點數高度                                                      |
| TextureCubeArray    | UINT MipLevel、UINT Width、UINT Height、UINT 元素、UINT NumberOfLevels     |
| TextureCubeArray    | UINT Width、UINT Height、UINT 元素                                         |
| TextureCubeArray    | UINT MipLevel、float Width、float Height、float Elements、float NumberOfLevels |
| TextureCubeArray    | 浮點數寬度、浮點數高度、浮點數元素                                      |
| Texture2DMS         | UINT 寬度、UINT 高度、UINT 樣本                                          |
| Texture2DMS         | 浮點數寬度、浮點數高度、浮點數範例                                       |
| Texture2DMSArray    | UINT 寬度、UINT Height、UINT 元素、UINT 範例                           |
| Texture2DMSArray    | 浮點數寬度、浮點數高度、浮點數元素、浮點數範例                       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  傳回最大 (第零個) mipmap 層級的維度。
2.  TextureCubeArray 適用于著色器模型4.1 或更高版本。
3.  在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





