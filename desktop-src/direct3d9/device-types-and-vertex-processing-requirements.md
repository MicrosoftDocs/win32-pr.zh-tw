---
description: 頂點處理作業的效能，包括轉換和光源，主要取決於頂點緩衝區存在於記憶體中的位置，以及正在使用的轉譯裝置類型。
ms.assetid: 4f9ca83d-c9d6-4749-944d-78f831b0f44e
title: " (Direct3D 9) 的裝置類型和頂點處理需求"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590cf2f5423d9c3bdf3e19c91f30b3e8c0586687
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510022"
---
# <a name="device-types-and-vertex-processing-requirements-direct3d-9"></a> (Direct3D 9) 的裝置類型和頂點處理需求

頂點處理作業的效能，包括轉換和光源，主要取決於頂點緩衝區存在於記憶體中的位置，以及正在使用的轉譯裝置類型。 應用程式在建立時，會控制頂點緩衝區的記憶體配置。 \_設定 D3DPOOL SYSTEMMEM memory 旗標時，會在系統記憶體中建立頂點緩衝區。 \_使用 D3DPOOL 預設記憶體旗標時，設備磁碟機會判斷頂點緩衝區的記憶體最適合配置的位置，通常稱為驅動程式優化的記憶體。 驅動程式-最佳的記憶體可以是本機視訊記憶體、非本機視訊記憶體或系統記憶體。

\_使用 [**IDirect3DDevice9：： CREATEVERTEXBUFFER**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)設定 D3DUSAGE SOFTWAREPROCESSING 常數可啟用頂點緩衝區資料的軟體頂點處理。 在混合模式中，軟體頂點處理需要此旗標。 旗標不可以用於硬體頂點處理模式。 與軟體頂點處理搭配使用的頂點緩衝區包括下列各項：

-   IDirect3DDevice9 的所有輸入資料流程 [**：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)。
-   IDirect3DDevice9 的所有輸入資料流程 [**：:D rawprimitive**](/windows/desktop/api) 和 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)。

您用來判斷記憶體位置（系統或驅動程式最佳）的原因，與紋理相同。 當頂點緩衝區配置在驅動程式優化的記憶體中，且軟體頂點處理最適合與系統記憶體中配置的頂點緩衝區搭配使用時，硬體中的頂點處理（包括轉換和光源）效果最好。 針對材質，當材質在驅動程式優化記憶體中配置時，硬體點陣化效果最好，而軟體點陣化與系統記憶體材質的效果最佳。

Microsoft Direct3D 9 支援對頂點的獨立處理，而不需要使用 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 方法來轉譯任何基本物件。 此獨立頂點處理一律會在主機處理器上的軟體中執行。 因此，使用 [**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api) 來設定來源的頂點緩衝區必須使用 D3DUSAGE SOFTWAREPROCESSING 旗標來建立 \_ 。 **IDirect3DDevice9：:P rocessvertices** 提供的功能與 [**IDirect3DDevice9：:D rawprimitive**](/windows/desktop/api)和 IDirect3DDevice9：在使用軟體頂點處理時 [**:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)方法相同。

如果您的應用程式會執行自己的頂點處理，並將轉換、發亮和裁剪的頂點傳遞給轉譯方法，則應用程式可以直接將頂點寫入至驅動程式優化記憶體中所配置的頂點緩衝區。 這項技術會防止稍後的冗餘複製作業。 請注意，如果您的應用程式從頂點緩衝區讀取資料，這項技術將無法正常運作，因為主機從驅動程式優化記憶體完成的讀取作業可能會非常緩慢。 因此，如果您的應用程式在處理過程中需要讀取，或將資料寫入緩衝區時，系統記憶體的頂點緩衝區是較佳的選擇。

使用 Direct3D 頂點處理功能 (藉由將未轉換頂點傳遞給頂點緩衝區轉譯方法) ，視裝置類型和裝置建立旗標而定，可能會在硬體或軟體中進行處理。 建議將頂點緩衝區配置在集區 D3DPOOL \_ 預設值，以在幾乎所有情況下獲得最佳效能。 當裝置使用硬體頂點處理時，有一些額外的優化可能會根據旗標 D3DUSAGE \_ DYNAMIC 和 D3DUSAGE WRITEONLY 來完成 \_ 。 如需有關使用這些旗標的詳細資訊，請參閱 IDirect3DDevice9：： CreateVertexBuffer。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點緩衝區](vertex-buffers.md)
</dt> </dl>

 

 
