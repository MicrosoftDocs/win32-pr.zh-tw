---
description: 以下是兩個範例二進位範本定義和一個二進位資料物件範例。
ms.assetid: vs|directx_sdk|~\examples.htm
title: " (Direct3D 9 圖形) 範例"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109161"
---
# <a name="examples-direct3d-9-graphics"></a><span data-ttu-id="69f44-103"> (Direct3D 9 圖形) 範例</span><span class="sxs-lookup"><span data-stu-id="69f44-103">Examples (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="69f44-104">以下是兩個範例二進位範本定義和一個二進位資料物件範例。</span><span class="sxs-lookup"><span data-stu-id="69f44-104">Two example binary template definitions and an example of a binary data object follow.</span></span>

> [!Note]  
> <span data-ttu-id="69f44-105">資料會以位元組由小到大的格式儲存，但不會顯示在這些範例中。</span><span class="sxs-lookup"><span data-stu-id="69f44-105">Data is stored in little-endian format, which is not shown in these examples.</span></span>

 

<span data-ttu-id="69f44-106">關閉的範本 RGB 是由 UUID {55b6d780-37ec-11d0-ab39-0020af71e433} 識別，且有三個成員-r、g 和 b-每個都是 float 類型。</span><span class="sxs-lookup"><span data-stu-id="69f44-106">The closed template RGB is identified by the UUID {55b6d780-37ec-11d0-ab39-0020af71e433} and has three members - r, g, and b - each of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



<span data-ttu-id="69f44-107">封閉式範本 Matrix4x4 是由 UUID {55b6d781-37ec-11d0-ab39-0020af71e433} 識別，且有一個成員-一維陣列，名為 float 類型的矩陣。</span><span class="sxs-lookup"><span data-stu-id="69f44-107">The closed template Matrix4x4 is identified by the UUID {55b6d781-37ec-11d0-ab39-0020af71e433} and has one member - a two-dimensional array named matrix - of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



<span data-ttu-id="69f44-108">接下來的二進位資料物件會顯示稍早定義的 RGB 範本實例。</span><span class="sxs-lookup"><span data-stu-id="69f44-108">The binary data object that follows shows an instance of the RGB template defined earlier.</span></span> <span data-ttu-id="69f44-109">範例物件的名稱是藍色，而它的三個成員（r、g 和 b）分別具有值0.0、0.0 和1.0。</span><span class="sxs-lookup"><span data-stu-id="69f44-109">The example object is named blue, and its three members - r, g, and b - have the values 0.0, 0.0, and 1.0, respectively.</span></span>


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a><span data-ttu-id="69f44-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="69f44-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f44-111">二進位編碼方式</span><span class="sxs-lookup"><span data-stu-id="69f44-111">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



