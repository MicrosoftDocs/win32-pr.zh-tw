---
description: 使用程式設計頂點著色器時，在目的地頂點緩衝區中更新的元素是由著色器函式程式所控制。
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: " (Direct3D 9) 的可程式化頂點處理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973949"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="493f5-103"> (Direct3D 9) 的可程式化頂點處理</span><span class="sxs-lookup"><span data-stu-id="493f5-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="493f5-104">使用程式設計頂點著色器時，在目的地頂點緩衝區中更新的元素是由著色器函式程式所控制。</span><span class="sxs-lookup"><span data-stu-id="493f5-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="493f5-105">當應用程式寫入其中一個目的地頂點暫存器時，會更新目的地頂點緩衝區中每個頂點內的對應元素。</span><span class="sxs-lookup"><span data-stu-id="493f5-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="493f5-106">不會修改目的地頂點緩衝區中不是由應用程式寫入的元素。</span><span class="sxs-lookup"><span data-stu-id="493f5-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="493f5-107">[**IDirect3DDevice9：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) 如果應用程式寫入的專案不存在於目的地頂點緩衝區中，:P rocessvertices 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="493f5-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="493f5-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="493f5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="493f5-109">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="493f5-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
