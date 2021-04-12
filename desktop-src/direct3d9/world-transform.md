---
description: 全球轉型的討論介紹基本概念，並提供如何設定全球轉換的詳細資料。
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: " (Direct3D 9) 的全球轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385602"
---
# <a name="world-transform-direct3d-9"></a> (Direct3D 9) 的全球轉換

全球轉型的討論介紹基本概念，並提供如何設定全球轉換的詳細資料。

## <a name="what-is-a-world-transform"></a>什麼是世界轉換？

「世界」轉換會從模型空間（其中頂點定義相對於模型的本機原點）到「世界空間」的座標，其中頂點的定義相對於場景中所有物件的原始來源。 簡單來說，世界矩陣轉換將模型放置到世界中；因此成為它的名字。 下圖顯示世界座標系統和模型區域座標系統之間的關係。

![世界座標及區域座標如何相關的簡圖](images/worldcrd.png)

世界矩陣轉換可以包含轉移、旋轉和縮放的任何組合。

## <a name="setting-up-a-world-matrix"></a>設定世界矩陣

如同任何其他轉換，藉由將一系列矩陣串連成一個包含效果總和的矩陣，建立世界矩陣轉換。 在最簡單的情形，當模型在世界原點，而且其區域座標軸的方向與世界空間相同時，世界矩陣是單位矩陣。 世界矩陣更常是轉移至世界空間以及可能一或多個旋轉 (視需要旋轉模型) 的組合。

下列範例會從以 c + + 撰寫的虛構3D 模型類別，使用 D3DX 公用程式程式庫中所包含的 helper 函式來建立世界矩陣，其中包含三個旋轉來定向模型，以及將其位置與其在世界空間中的位置相對應。


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



當您準備世界矩陣之後，請呼叫 [**IDirect3DDevice9：： SetTransform**](/windows/desktop/api) 方法來設定它，並指定第一個參數的 [**D3DTS \_ world**](d3dts-world.md) 宏。

> [!Note]  
> Direct3D 使用世界和檢視矩陣，讓您設定數個內部資料結構。 每當您設定世界或檢視矩陣，系統會重新計算相關內部結構。 頻繁設定這些矩陣 (例如，每個畫面數千次) 通常在計算上耗費時間。 您可以串連世界和檢視矩陣成為世界檢視矩陣 (您將其設為世界矩陣)，然後將檢視矩陣設為單位矩陣，將所需的計算次數最小化。 保留個別世界和檢視矩陣的快取複本，讓您可以視需要修改、串連並重設世界矩陣。 為了清楚起見，在本檔中，Direct3D 範例很少使用這項優化。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換](transforms.md)
</dt> </dl>

 

 



