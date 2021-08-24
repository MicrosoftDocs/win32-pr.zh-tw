---
description: 材質管理是判斷在指定時間轉譯需要哪些材質的程式，並確保將這些材質載入視訊記憶體中。
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: '自動材質管理 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c65168947acb05c8437836ba0b27765a9b03d3ba97fd223f50eb9a99ab8c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751398"
---
# <a name="automatic-texture-management-direct3d-9"></a>自動材質管理 (Direct3D 9) 

材質管理是判斷在指定時間轉譯需要哪些材質的程式，並確保將這些材質載入視訊記憶體中。 如同任何演算法，材質管理配置會因複雜性而異，但任何材質管理方法都牽涉到下列重要工作。

-   追蹤可用材質記憶體的數量。
-   計算轉譯所需的材質，而不需要。
-   判斷哪些現有的材質資源可以使用另一個材質影像重載，以及應終結哪些表面，並以新的材質資源取代。

Direct3D 會實行系統支援的材質管理，以確保載入紋理以獲得最佳效能。 Direct3D 管理的材質資源稱為 managed 紋理。

材質管理員會追蹤具有時間戳記的材質，以識別上次使用材質的時間戳記。 然後，它會使用最少最近使用的演算法來判斷應該移除的材質。 當有兩個紋理的目標是要從記憶體中移除時，材質優先順序會用來做為系結器。 如果兩個材質具有相同的優先順序值，則會移除最近最少使用的材質。 但是，如果兩個材質具有相同的時間戳記，則會先移除優先順序較低的材質。

當您建立紋理介面時，會要求自動材質管理。 若要在 c + + 應用程式中取出 managed 材質，請呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 並指定為集區參數所管理的 D3DPOOL，以建立材質資源 \_ 。 您不能指定要建立紋理的位置。 當您建立 managed 材質時，不能使用 D3DPOOL \_ DEFAULT 或 D3DPOOL \_ SYSTEMMEM 旗標。 建立 managed 材質之後，您可以呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，將其設定為轉譯裝置材質串聯中的階段。

您可以針對材質介面呼叫 [**IDirect3DResource9：： SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) 方法，將優先順序指派給 managed 紋理。

Direct3D 會視需要自動將材質下載至視訊記憶體。 系統可能會將受控紋理快取在本機或非本機的視訊記憶體中，視非本機視訊記憶體的可用性或其他因素而定。 受控紋理的快取位置不會傳達給您的應用程式，也不需要使用自動材質管理的這項資訊。 如果您的應用程式使用的紋理多於可容納在視頻記憶體中的材質，Direct3D 會從視訊記憶體中移除較舊的材質，以騰出空間給新的材質。 如果您再次使用移除的材質，系統會使用原始的系統記憶體紋理介面，在視訊記憶體快取中重載紋理。 雖然需要重載紋理，但它也會降低應用程式的效能。

您可以藉由更新或鎖定材質資源，以動態方式修改紋理的原始系統記憶體複本。 當系統偵測到中途的介面時，在更新完成之後或介面解除鎖定時，材質管理員會自動更新材質的視訊記憶體複本。 產生的效能影響類似于重載移除的材質。

在遊戲中輸入新的層級時，您的應用程式可能需要藉由呼叫 [**IDirect3DDevice9：： EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)) ，來排清視訊記憶體 (中的所有 managed 紋理。

如需資源管理的詳細資訊，請參閱 [管理資源 (Direct3D 9) ](managing-resources.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
