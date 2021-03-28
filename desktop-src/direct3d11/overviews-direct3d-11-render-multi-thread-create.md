---
title: 使用多執行緒建立物件
description: 您可以使用 ID3D11Device 介面來建立資源和物件，並使用 >id3d11devicecoNtext 來呈現。
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932237"
---
# <a name="object-creation-with-multithreading"></a>使用多執行緒建立物件

您可以使用 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面來建立資源和物件，並使用 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 來 [呈現](overviews-direct3d-11-render-multi-thread-render.md)。

以下是如何建立資源的一些範例：

-   [如何：建立頂點緩衝區](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [如何：建立索引緩衝區](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [如何：建立常數緩衝區](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [如何：從檔案初始化材質](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>多執行緒考慮

您的應用程式可達成的資源建立和轉譯的平行存取量，取決於驅動程式所實行的多執行緒支援層級。 如果驅動程式支援並行建立，則應用程式應該會有較少的平行存取考慮。 但是，如果驅動程式不支援並行物件建立，則平行存取量非常有限。 若要瞭解驅動程式中可用的支援數量，請查詢驅動程式以取得 [**D3D11 \_ 功能 \_ 資料 \_ 執行緒**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading)結構的 **DriverConcurrentCreates** 成員的值。 如需有關檢查多執行緒的驅動程式支援的詳細資訊，請參閱 [如何：檢查驅動程式支援](overviews-direct3d-11-render-multi-thread-support.md)。

並行作業不一定會導致效能較佳。 例如，建立及載入紋理通常會受到記憶體頻寬的限制。 即使這會讓多個 CPU 核心閒置，嘗試建立和載入多個紋理的速度可能會比一次執行一個材質的速度還快。 不過，使用多個執行緒建立多個著色器可能會提高效能，因為這項作業較不依賴系統資源（例如記憶體頻寬）。

當驅動程式和圖形硬體支援多執行緒時，您通常可以藉由將指標傳遞至 *pInitialData* 參數中的初始資料，以更有效率地初始化新建立的資源 (例如，在 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 方法的呼叫中) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多執行緒](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




