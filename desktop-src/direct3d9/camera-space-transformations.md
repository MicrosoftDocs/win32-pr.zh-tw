---
description: 相機空間端點的計算方式為使用全球檢視矩陣轉換物件端點。
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: " (Direct3D 9) 的相機空間轉換"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110768"
---
# <a name="camera-space-transformations-direct3d-9"></a> (Direct3D 9) 的相機空間轉換

相機空間端點的計算方式為使用全球檢視矩陣轉換物件端點。

V = V \* wvMatrix

相機空間頂點標準的計算方式為，使用全球檢視矩陣的反向調換來轉換物件標準。 全球檢視矩陣不一定是正交。

N = N \* (wvMatrix ⁻¹) <sup>T</sup>

矩陣反向和矩陣調換於4 x 4 矩陣運作。 乘積結合標準與產出之 4 x 4 矩陣的 3 x 3 部分。

如果轉譯狀態 D3DRENDERSTATE \_ NORMALIZENORMALS 設定為 **TRUE**，則會在轉換成相機空間之後，將頂點標準向量正規化，如下所示：

N = norm(N)

相機空間光線位置的計算方式為，使用檢視矩陣轉換光線來源位置。

Lp = Lp \* vMatrix

相機空間光線方向的計算方式為，將光線來源方向乘以檢視矩陣、正規化以及取補數結果。

L<sub>dir</sub> =-標準 (L<sub>dir</sub> \* wvMatrix) 

若為 D3DLIGHT \_ 點和 D3DLIGHT 點，則會以下列 \_ 方式計算燈的方向：

L<sub>dir</sub> = 標準 (的 \*) ，其中參數定義于下表中。



| 參數       | 預設值 | 類型      | Description                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| L<sub>dir</sub> | N/A           | D3DVECTOR | 從物件頂點到光線的方向向量          |
| V               | N/A           | D3DVECTOR | 相機空間的頂點位置                           |
| wvMatrix        | 身分識別      | D3DMATRIX | 複合矩陣包含全球及檢視轉換 |
| N               | N/A           | D3DVECTOR | 頂點垂直                                             |
| Lₚ              | N/A           | D3DVECTOR | 相機空間的光線位置                            |
| vMatrix         | 身分識別      | D3DMATRIX | 矩陣包含檢視轉換                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[燈光數學](mathematics-of-lighting.md)
</dt> </dl>

 

 



