---
description: 雖然詞彙寬度和音調通常是非正式使用的，但它們具有非常重要且意義截然不同的意義。 因此，您應該瞭解每個專案的意義，以及如何解讀 Direct3D 用來描述這些值的值。
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: '寬度與音調 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1c697ec4c9278a78a5539818b30038d99fc9d59d96af7f22ee87c33949abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095510"
---
# <a name="width-vs-pitch-direct3d-9"></a>寬度與音調 (Direct3D 9) 

雖然詞彙寬度和音調通常是非正式使用的，但它們具有非常重要且意義截然不同的意義。 因此，您應該瞭解每個專案的意義，以及如何解讀 Direct3D 用來描述這些值的值。

Direct3D 使用 [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) 結構來傳送描述介面的資訊。 除此之外，此結構的定義是要包含表面維度的相關資訊，以及這些維度在記憶體中的表示方式。 結構會使用高度和寬度成員來描述介面的邏輯維度。 這兩個成員都是以圖元為單位。 因此，640 x 480 表面的高度和寬度值都相同，無論是8位介面或24位 RGB 表面。

當您使用 [**IDirect3DSurface9：： LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 方法鎖定介面時，此方法會填入 [**D3DLOCKED \_ RECT**](d3dlocked-rect.md) 結構，其中包含介面的音調和鎖定位的指標。 螺距成員中的值會描述表面的記憶體音調，也稱為 stride。 「音調」是兩個記憶體位址之間的距離（以位元組為單位），代表一個點陣圖線的開頭和下一個點陣圖行的開頭。 由於音調以位元組為單位來測量，而不是以圖元為單位，因此640x480x8 介面的音調值會與具有相同維度但不同像素格式的介面非常不同。 此外，量值有時會反映 Direct3D 已保留為快取的位元組，因此不安全的方式是將該音調的寬度乘以每個圖元的位元組數目。 相反地，將寬度和音調的差異視覺化，如下圖所示。

![相同前端緩衝區、背景緩衝區和快取的音調和寬度圖表](images/pitch.png)

在此圖中，前端緩衝區和背景緩衝區都是640x480x8，而且快取為384x480x8。

直接存取介面時，請小心保持在配置給表面維度的記憶體內，並將任何保留給快取的記憶體保持不變。 此外，當您只鎖定部分的介面時，您必須保持在鎖定介面時所指定的矩形內。 若無法遵循這些指導方針，將會產生無法預期的結果。 直接轉譯成 surface memory 時，請一律使用 [**IDirect3DSurface9：： LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) 方法所傳回的音調。 請勿假設只以顯示模式為基礎的音調。 如果您的應用程式適用于某些顯示器介面卡，但在其他情況下看起來很模糊，這可能是問題的原因。

如需詳細資訊，請參閱 [直接存取 (Direct3D 9) 的介面記憶體 ](accessing-surface-memory-directly.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 
