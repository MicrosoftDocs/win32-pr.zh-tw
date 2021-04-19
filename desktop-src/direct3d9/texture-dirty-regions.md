---
description: 應用程式可以藉由指定 &\# 0034; 變更&\# 0034; 材質上的區域，優化複製材質的子集。
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: " (Direct3D 9) 的材質中途區域"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970694"
---
# <a name="texture-dirty-regions-direct3d-9"></a> (Direct3D 9) 的材質中途區域

應用程式可以在紋理上指定「已變更」區域，以優化材質的子集複製。 只有標記為中途的區域會透過呼叫 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)來複製。 不過，可能會擴充中途區域以優化對齊。 建立材質時，會將整個材質視為中途變更。 只有下列作業會影響材質的變更狀態：

-   將中途區域新增至材質。
-   鎖定材質中的一些緩衝區。 此作業會將鎖定的區域新增為中途區域。 如果應用程式對實際的中途區域有更好的瞭解，就可以關閉此自動變更區域更新。
-   使用紋理的介面層級做為 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) 中的目的地，會將整個材質標示為中途。
-   在 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 中使用材質作為來源，會清除來源材質上的所有中途區域。
-   使用 [**IDirect3DSurface9：： GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) 傳回裝置內容。
-   呼叫 [**IDirect3DBaseTexture9：： GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) 會將整個材質標示為中途。
-   呼叫 [**IDirect3DBaseTexture9：： SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) 會將整個材質標示為中途。

中途區域是在 mipmapped 材質的最上層設定，而 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 可將中途區域展開至 mip 鏈，以將每個子層級複製的位元組數目降至最低。 請注意，子層中途區域座標會向外舍入，也就是說，其小數部分會舍入至最接近紋理的邊緣。

由於每種材質類型都有不同類型的中途區域，因此每個材質類型都有方法。 2D 紋理使用中途矩形，以及大量紋理使用方塊。

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

針對上述方法傳遞 **Null** 作為 PDirtyRect 或 pDirtyBox 參數，會展開中途區域以涵蓋整個材質。

每個鎖定方法都可以 D3DLOCK \_ 沒有中途 \_ \_ 更新，這可防止材質的變更狀態變更。 如需詳細資訊，請參閱 [ (Direct3D 9) 的鎖定資源 ](locking-resources.md)。

如果有關于在鎖定作業期間變更之真組區域的詳細資訊，應用程式應該使用 D3DLOCK \_ NO \_ DIRTY \_ UPDATE。 請注意，只有在不鎖定或複製到最上層) 的情況下，才會鎖定或複製材質子層 (也不會更新該材質的中途區域。 當應用程式鎖定較低的層級，而不鎖定最上層時，應用程式會採用相同的責任來更新中途區域。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本紋理概念](basic-texturing-concepts.md)
</dt> </dl>

 

 
