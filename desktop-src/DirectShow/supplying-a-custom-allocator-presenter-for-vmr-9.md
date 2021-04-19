---
description: 提供 VMR-9 的自訂 Allocator-Presenter
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: 提供 VMR-9 的自訂 Allocator-Presenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987808"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>提供 VMR-9 的自訂 Allocator-Presenter

若要搭配影片混合轉譯器 9 (VMR-9) 篩選器來使用自訂配置器提供者，請執行下列步驟：

1.  執行支援 [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) 和 [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) 介面的類別。
2.  針對 [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)介面，在 VMR-9 篩選器上呼叫 **QueryInterface** 。
3.  呼叫 [**IVMRFilterConfig9：： SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) 方法，並傳入 **VMR9Mode \_ Renderless** 旗標。
4.  [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)介面的 VMR-9 篩選器上的 **QueryInterface** 。
5.  呼叫 [**IVMRSurfaceAllocatorNotify9：： AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) 方法，並將指標傳入配置器展示者的 [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) 方法。
6.  呼叫您配置器的 [**IVMRSurfaceAllocator9：： AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) 方法，並將指標傳入 VMR 9 篩選器的 [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) 介面。
7.  在您的 [**IVMRSurfaceAllocator9：： AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify)的執行中，呼叫 [**IVMRSurfaceAllocatorNotify9：： SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) ，並將指標放在 Direct3D 裝置的指標，以及顯示影片的監視器控制碼。
8.  在您的 [**IVMRSurfaceAllocator9：： InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) 方法的執行中，建立符合 **InitializeDevice** 方法中指定之參數的 Direct3D 表面。 （選擇性）您可以使用 VMR-9 篩選的 [**IVMRSurfaceAllocatorNotify9：： AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) 方法來配置這些表面。 將介面指標儲存在陣列中。
    > [!Note]  
    > 如果您想要 VMR-9 將影片框架繪製到材質介面上，請將 **VMR9AllocFlag \_ TextureSurface** 旗標新增至 [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) 結構。 如果裝置不支援原生影片格式的紋理，您可能需要建立個別的材質介面，然後將影片畫面從影片表面複製到材質。

     

9.  在串流處理期間，VMR-9 會藉由呼叫 [**IVMRSurfaceAllocator9：： GetSurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) 方法，從配置器呈現器取得介面。 VMR-9 會依照介面陣列中的索引來指定介面 (步驟 8) 。
10. 當 VMR-9 呼叫 [**IVMRImagePresenter9：:P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) 方法時，呈現映射。 這些參數包含包含影片影像的 Direct3D 介面指標。
11. 如果 Direct3D 裝置隨時遺失，配置器展示者必須還原裝置，並重新建立這些表面。 例如，如果顯示模式變更或使用者將視窗移到另一個監視器，則裝置可能會遺失。 如果 Direct3D 裝置變更，請呼叫 VMR-9 篩選器的 [**IVMRSurfaceAllocatorNotify9：： ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) 方法。
12. 當串流停止時，VMR-9 會呼叫 [**IVMRSurfaceAllocator9：： TerminateDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) 方法。 配置器-展示者應該釋放其所有的 Direct3D 資源。

在自訂配置器-管理者的管理方式中，VMR-7 和 VMR-9 之間有一些差異：

-   VMR-9 篩選器的 [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) 方法可供配置器提供者在配置表面時使用。 這種方法不需要讓自訂配置器提供者將任何呼叫轉送到預設配置器-展示者。 基於這個理由，不會發行 VMR 9 篩選器預設配置器的 CLSID。
-   不同于 VMR-7，VMR-9 不提供特殊的 DirectDraw 專屬模式配置器-展示者。 [**IVMRSurfaceAllocatorNotify9：： AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper)方法會讓此物件不需要。
-   針對交錯式影片，VMR-9 一律會在顯示影像之前，先將影片取消 interlaces。 配置器-展示者不再負責在顯示影像之前將影像取消交錯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VMR Renderless 播放模式 (自訂配置器-展示者) ](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



