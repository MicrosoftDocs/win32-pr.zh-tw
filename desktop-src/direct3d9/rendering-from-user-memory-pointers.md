---
description: 一組次要的轉譯介面支援直接從使用者記憶體指標傳遞頂點和索引資料。 這些介面僅支援頂點資料的單一資料流程。 如需詳細資訊，請參閱下列參考主題。
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: '從使用者記憶體指標轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187508"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a>從使用者記憶體指標轉譯 (Direct3D 9) 

一組次要的轉譯介面支援直接從使用者記憶體指標傳遞頂點和索引資料。 這些介面僅支援頂點資料的單一資料流程。 如需詳細資訊，請參閱下列參考主題。

-   [**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

這些方法會使用使用者記憶體指標所指定的資料來呈現，而不是使用頂點和索引緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現基本專案](rendering-primitives.md)
</dt> </dl>

 

 
