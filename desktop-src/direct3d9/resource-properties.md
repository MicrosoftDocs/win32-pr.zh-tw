---
description: 所有資源都會共用下列屬性。
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: " (Direct3D 9) 的資源屬性"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688260"
---
# <a name="resource-properties-direct3d-9"></a> (Direct3D 9) 的資源屬性

所有資源都會共用下列屬性。

-   使用狀況。 使用資源的方式，例如，作為材質或轉譯目標。
-   格式化。 資料的格式，例如2D 介面的像素格式。
-   池。 配置資源的記憶體類型。
-   輸入 。 資源的類型，例如頂點緩衝區或轉譯目標。

系統會強制執行資源使用。 將在特定作業中使用資源的應用程式，必須在資源建立時間指定該操作。 如需為資源定義的使用常數清單，請參閱 [**D3DUSAGE**](d3dusage.md)。

D3DUSAGE \_ RTPATCHES、D3DUSAGE \_ NPATCHES 和 D3DUSAGE point \_ 常數向驅動程式指出，這些緩衝區中的資料可能會分別用於三角形或方格修補程式、N 修補程式或分階段。 系統會提供這些旗標，以防硬體無法在未進行主機處理的情況下執行這些作業。 因此，驅動程式會想要在系統記憶體中配置這些表面，讓 CPU 可以存取它們。 如果驅動程式可以完全在硬體中執行這些作業，它就可以在影片或 AGP 記憶體中配置這些表面，以避免主機複本，並提高效能至少兩次。 請注意，這些旗標所提供的資訊並不是絕對必要的。 驅動程式可以偵測到這類作業正在資料上執行，而且會將緩衝區移回系統記憶體以供後續的框架使用。

如需使用方式旗標的詳細資訊，以及它們與特定資源之間的關聯性，請參閱個別資源建立方法上的參考頁面。

如需有關資源表面格式的詳細資訊，請參閱 [D3DFORMAT](d3dformat.md) 列舉型別。

保存資源緩衝區的記憶體類別稱為「集區」。 集區值是由 [**D3DPOOL**](./d3dpool.md) 列舉類型所定義。 針對單一資源中包含的不同物件（也就是 mipmap 中的 mip 層級），不能混用集區，而且當為資源選擇集區時，無法變更集區。

當應用程式呼叫資源建立方法（例如 [**IDirect3DDevice9：： CreateCubeTexture**](/windows/desktop/api)）時，這些資源類型會在執行時間隱含設定。 資源類型是由 [**D3DRESOURCETYPE**](./d3dresourcetype.md) 列舉類型所定義。 應用程式可以在執行時間查詢這些類型;不過，大部分案例都不需要執行時間類型檢查。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> </dl>

 

 
