---
description: 您可以使用 IDirect3DSurface9：： LockRect 方法，直接存取 surface 記憶體。
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: 直接存取 (Direct3D 9) 的介面記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317864"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>直接存取 (Direct3D 9) 的介面記憶體

您可以使用 [**IDirect3DSurface9：： LockRect**](/windows/desktop/api) 方法，直接存取 surface 記憶體。 當您呼叫這個方法時，pRect 參數是 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構的指標，可描述介面上要直接存取的矩形。 若要要求鎖定整個介面，請將 pRect 設定為 **Null**。 此外，您也可以指定只涵蓋介面一部分的 **矩形** 。 如果沒有兩個矩形重迭，則兩個執行緒或進程可以同時鎖定介面中的多個矩形。 請注意，無法鎖定多級取樣背景緩衝區。

[**IDirect3DSurface9：： LockRect**](/windows/desktop/api)方法會以所有資訊填入 [**D3DLOCKED \_ RECT**](d3dlocked-rect.md)結構，以適當地存取介面記憶體。 結構包含了有關音調的資訊，並且具有鎖定位的指標。 當您完成介面記憶體的存取時，請呼叫 [**IDirect3DSurface9：： UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) 方法將它解除鎖定。

當您鎖定了介面時，可以直接操作內容。 下列清單描述一些可避免直接呈現介面記憶體常見問題的秘訣。

-   絕對不要採用常數顯示音調。 一律檢查 [**IDirect3DSurface9：： LockRect**](/windows/desktop/api) 方法所傳回的音調資訊。 這種方式可能會因許多原因而有所不同，包括介面記憶體的位置、顯示配接器類型，或甚至是 Direct3D 驅動程式的版本。 如需詳細資訊，請參閱 [Width 與音調 (Direct3D 9) ](width-vs--pitch.md)。
-   確定您已複製到未鎖定的表面。 如果在鎖定的介面上呼叫，Direct3D 複製方法將會失敗。
-   鎖定介面時限制應用程式的活動。
-   一律複製對齊顯示記憶體的資料。 Windows 98 使用分頁錯誤處理常式（Vflatd）來針對具有 bank 切換記憶體的顯示器卡片，執行虛擬的一般框架緩衝區。 此處理程式可讓這些顯示裝置對 Direct3D 呈現線性框架緩衝區。 將未配置的資料複製到顯示記憶體，可能會導致系統在複本跨越記憶體 bank 時暫停作業。
-   如果介面屬於指派給 D3DPOOL 預設記憶體集區的資源，則介面可能無法鎖定， \_ 除非它是動態材質或使用 [**IDirect3DDevice9：： CreateOffscreenPlainSurface**](/windows/desktop/api)建立的介面。 您可以使用 [**IDirect3DDevice9：： GetBackBuffer**](/windows/desktop/api) 和 [**IDirect3DSwapChain9：： GetBackBuffer**](/windows/desktop/api) 方法存取的背景緩衝區介面，只有在使用 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 的旗標成員建立交換鏈，以包含 D3DPRESENTFLAG 可鎖定背景緩衝區時，才會鎖定 \_ \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 表面](direct3d-surfaces.md)
</dt> </dl>

 

 
