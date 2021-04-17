---
description: 下列檔案會定義具有四個紅邊和兩個綠色邊的簡單 cube。 在這個檔案中，選擇性資訊是用來將資訊新增至網格範本所定義的資料物件。
ms.assetid: 310981bf-3536-43dd-ad7c-40ab6c8ef6c4
title: '定義簡單的 Cube (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d92d1b97a16e3a26f58281f9621282d3bdc487
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467443"
---
# <a name="defining-a-simple-cube-direct3d-9"></a>定義簡單的 Cube (Direct3D 9) 

下列檔案會定義具有四個紅邊和兩個綠色邊的簡單 cube。 在這個檔案中，選擇性資訊是用來將資訊新增至 [**網格**](mesh.md) 範本所定義的資料物件。


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
}

// Define a mesh with 8 vertices and 12 faces (triangles). Use 
// optional data objects in the mesh to specify materials, normals,
// and texture coordinates.
Mesh CubeMesh {
8;                                // 8 vertices.
1.000000;1.000000;-1.000000;,     // Vertex 0.
-1.000000;1.000000;-1.000000;,    // Vertex 1.
-1.000000;1.000000;1.000000;,     // And so on.
1.000000;1.000000;1.000000;,
1.000000;-1.000000;-1.000000;,
-1.000000;-1.000000;-1.000000;,
-1.000000;-1.000000;1.000000;,
1.000000;-1.000000;1.000000;;

12;                      // 12 faces.
3;0,1,2;,                // Face 0 has three vertices.
3;0,2,3;,                // And so on.
3;0,4,5;,
3;0,5,1;,
3;1,5,6;,
3;1,6,2;,
3;2,6,7;,
3;2,7,3;,
3;3,7,4;,
3;3,4,0;,
3;4,7,6;,
3;4,6,5;;

// All required data has been defined. Now define optional data
// using the hierarchical nature of the file format.
MeshMaterialList {
2;                    // Number of materials used.
12;                   // A material for each face.
0,                    // Face 0 uses the first material.
0,
0,
0,
0,
0,
0,
0,
1,                    // Face 8 uses the second material.
1,
1,
1;;
{RedMaterial}         // References to the definitions
{GreenMaterial}       // of material 0 and 1.
}
MeshNormals {
8;                    // Define 8 normals.
0.333333;0.666667;-0.666667;,
-0.816497;0.408248;-0.408248;,
-0.333333;0.666667;0.666667;,
0.816497;0.408248;0.408248;,
0.666667;-0.666667;-0.333333;,
-0.408248;-0.408248;-0.816497;,
-0.666667;-0.666667;0.333333;,
0.408248;-0.408248;0.816497;;
12;                   // For the 12 faces, define the normals.
3;0,1,2;,
3;0,2,3;,
3;0,4,5;,
3;0,5,1;,
3;1,5,6;,
3;1,6,2;,
3;2,6,7;,
3;2,7,3;,
3;3,7,4;,
3;3,4,0;,
3;4,7,6;,
3;4,6,5;;
}
MeshTextureCoords {
8;                        // Define texture coords for each vertex.
0.000000;1.000000;
1.000000;1.000000;
0.000000;1.000000;
1.000000;1.000000;
0.000000;0.000000;
1.000000;0.000000;
0.000000;0.000000;
1.000000;0.000000;;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[X 檔案 (舊版) ](x-files--legacy-.md)
</dt> </dl>

 

 



