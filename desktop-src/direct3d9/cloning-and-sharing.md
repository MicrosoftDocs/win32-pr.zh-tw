---
description: '複製和共用 (Direct3D 9) '
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: '複製和共用 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96add856c6e3c675cbf3ac225d39517214ed9dc002abded6f4f7f9f75d4736bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857698"
---
# <a name="cloning-and-sharing-direct3d-9"></a>複製和共用 (Direct3D 9) 

## <a name="cloning-parameters"></a>複製參數

複製有下列限制。

-   複製會繼承原始效果的集區。 請參閱共用參數一節。
-   複製會繼承原始效果的技術、傳遞、參數和注釋 (包括以 [**ID3DXEffect**](id3dxeffect.md)) 新增的所有批註。
-   複製會繼承原始效果動態加入的注釋。
-   如果原始效果的集區不是 **Null** ，而且原始效果包含共用裝置相依參數 (例如紋理或著色器) ，則複製到新裝置上的作業將會失敗。

## <a name="sharing-parameters"></a>共用參數

集區是在不同效果之間共用效果參數的緩衝區。 若要將參數新增至集區，請在建立效果時指定共用的使用方式。

集區具有下列限制。

-   第一次將包含該 (共用) 參數的效果新增至集區時，會將參數新增至集區。
-   集區會從第一個共用參數取得初始值;之後共用的參數會從集區中取得其值。
-   當共用參數的所有效果參考都釋出時，就會從集區刪除參數。
-   集區中包含相同 (共用) 裝置相依參數的所有效果都必須有相同的裝置。

**Null** 可以用來指定沒有集區，在此情況下不會共用任何參數。 這幾乎相當於僅針對此效果指定唯一的集區。 唯一的差異在於複製效果時，複製不會與原始的共用參數共用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



