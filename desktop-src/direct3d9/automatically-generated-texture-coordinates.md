---
title: '自動產生的材質座標 (Direct3D 9) '
description: 系統可以使用已轉換的相機空間位置或頂點中的法線作為材質座標，也可以計算用來定址三個元素向量的三個元素向量。
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997070"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>自動產生的材質座標 (Direct3D 9) 

系統可以使用已轉換的相機空間位置或頂點中的法線作為材質座標，也可以計算用來定址三個元素向量的三個元素向量。 如同您在頂點中明確指定的材質座標，您可以使用自動產生的材質座標作為材質座標轉換的輸入。

自動產生的材質座標可以大幅減少幾何資料所需的頻寬，方法是消除頂點格式的明確材質座標需求。 在許多情況下，系統產生的材質座標可以搭配轉換使用，以產生特殊效果。 當然，這是一個特殊用途的功能，而且您會在許多情況下使用明確的材質座標。

## <a name="configuring-automatically-generated-texture-coordinates"></a>設定自動產生的材質座標

在 c + + 中， \_ [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別中的 D3DTSS TEXCOORDINDEX 材質階段狀態 (，) 控制系統產生材質座標的方式。

一般來說，此狀態會指示系統使用以頂點格式編碼的一組特定紋理座標。 當您 \_ 將 D3DTSS TCI \_ CAMERASPACENORMAL、D3DTSS \_ TCI \_ CAMERASPACEPOSITION 或 D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR 旗標包含在指派給此狀態的值中時，系統行為會相當不同。 如果有任何這些旗標存在，紋理階段會忽略頂點格式內的材質座標，以配合系統所產生的座標。 下列清單會顯示每個旗標的意義。

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    使用轉換成相機空間的頂點，作為輸入材質座標。

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    使用頂點位置（轉換成相機空間）做為輸入材質座標。

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    使用轉換成相機空間的反映向量做為輸入材質座標。 反映向量是從輸入頂點位置和一般向量計算而來。

材質座標索引旗標是互斥的。 這個範例會使用：

-   [相機空間] (的頂點位置) 為此材質階段的輸入材質座標
-   D3DRENDERSTATE WRAP1 轉譯狀態中設定的 wrap 模式 \_


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



自動產生的材質座標最適合作為紋理座標轉換的輸入值，或讓應用程式不需要計算三個元素的三個元素向量來進行三個元素的對應。

球體對應會在模型時間使用預先計算 () 材質圖，其中包含由 chrome 球體反映的整個環境。 Direct3D 具有使用轉譯狀態 D3DTSS TCI CAMERASPACENORMAL 的材質座標產生功能，此功能 \_ \_ 會採用相機空間中頂點的標準，並透過材質轉換來產生材質座標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質座標處理](texture-coordinate-processing.md)
</dt> <dt>

[ (Direct3D 9) 的材質座標轉換 ](texture-coordinate-transformations.md)
</dt> <dt>

[ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)
</dt> </dl>

 

 
