---
title: 如何以程式設計方式初始化材質
description: 本主題包含數個範例，示範如何初始化使用不同類型的使用方式所建立的材質。
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b7d34e7e85fd647a6f45c93d61b3330825261f59d87b9c13a95547e742e365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530560"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>如何：以程式設計方式初始化材質

您可以在物件建立期間初始化材質，也可以在建立物件之後，以程式設計的方式填入該物件。 本主題包含數個範例，示範如何初始化使用不同類型的使用方式所建立的材質。 此範例假設您已經知道如何 [建立材質](overviews-direct3d-11-resources-textures-create.md)。

-   [預設使用方式](#default-usage)
-   [動態使用方式](#dynamic-usage)
-   [暫存使用量](#staging-usage)
-   [相關主題](#related-topics)

## <a name="default-usage"></a>預設使用方式

最常見的使用類型是預設使用方式。 若要填滿預設材質 (使用 **D3D11 \_ \_ 預設值** 建立的材質) 您可以：

-   呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 並初始化 *pInitialData* ，以指向應用程式所提供的資料。

    或

-   呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)之後，請使用 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ，將來自應用程式所提供之指標的資料填入預設材質。

## <a name="dynamic-usage"></a>動態使用方式

若要填滿動態材質 (使用 **\_ \_ 動態** 材質建立的) ：

1.  藉由在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時傳遞 **D3D11 \_ 對應 \_ 寫入 \_ 捨棄**，來取得材質記憶體的指標。
2.  將資料寫入記憶體。
3.  當您完成寫入資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應。

## <a name="staging-usage"></a>暫存使用量

若要填入預備材質 (使用 **D3D11 \_ 使用量 \_ 暫存**) 建立一個：

1.  在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時傳遞 **D3D11 \_ MAP \_ WRITE** ，以取得紋理記憶體的指標。
2.  將資料寫入記憶體。
3.  當您完成寫入資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應。

接下來可以使用預備紋理作為 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 或 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 的來源參數，以填滿預設或動態的資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[紋理](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




