---
title: 適用于 Direct3D 12 的 Helper 結構和函式
description: 這些 helper 結構和 helper 函數是在中宣告 `d3dx12.h` 。
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Helper 函式
- Helper 結構
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812174"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>適用于 Direct3D 12 的 Helper 結構和函式

這些 helper 結構和 helper 函數是在中宣告 `d3dx12.h` 。

`d3dx12.h` 可以與 Direct3D 12 標頭分開使用。 您可以 `d3dx12.h` 從 [D3D12 Helper 程式庫](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)進行下載。

您可以使用這些 helper 結構來建立和初始化 Direct3D 結構。 這些 helper 結構的行為就像 c + + 類別一樣。 每個 helper 結構通常都有一個預設的函式、一個明確的函式、一個函式，以及相關聯 D3D12 結構的 cast 運算子。 每個協助程式結構都有 ' C ' 前置詞，而且與缺少 ' C ' 前置詞的 D3D12 結構相關聯。 大部分的協助程式結構都包含初始化成員方法，有些則包含比較函數。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [D3D12 的 Helper 介面](helper-interfaces-for-d3d12.md) | 這些 helper 介面特別有助於處理子資源，而且會在中宣告 `d3dx12.h` 。  |
| [D3D12 的 Helper 結構](helper-structures-for-d3d12.md) | 這些 helper 結構有助於初始化許多 Direct3D 12 結構，並在中宣告 `d3dx12.h` 。 |
| [D3D12 的 Helper 函式](helper-functions-for-d3d12.md) | 這些 helper 函式有助於處理子資源，而且會在中宣告 `d3dx12.h` 。  |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 參考](direct3d-12-reference.md)
