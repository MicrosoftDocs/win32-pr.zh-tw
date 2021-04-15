---
description: 提供 VMR-7 的自訂 Allocator-Presenter
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: 提供 VMR-7 的自訂 Allocator-Presenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554893"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>提供 VMR-7 的自訂 Allocator-Presenter

配置器-展示者負責配置 DirectDraw 表面，並呈現影片框架以供轉譯。 在大部分的案例中，預設配置器的功能會比應用程式的需求還多。 但是，藉由插入自訂配置器提供者，應用程式可以直接存取影片位，並且完全控制轉譯流程。 這項增強功能的代價是，應用程式必須處理額外的 DirectDraw 介面管理複雜性。

![使用自訂配置器-展示者](images/custom-ap.png)

上圖顯示 VMR 和配置器展示者所使用的通訊介面。 覆寫所有預設配置和呈現功能的自訂配置器呈現者，必須執行 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 和 [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) 介面，也可以選擇 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)。

為了取代預設配置器-展示者，應用程式會呼叫 [**IVMRSurfaceAllocatorNotify：： AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) 方法，並將指標傳遞給新的配置器-展示者。 為了回應此呼叫，VMR 會呼叫配置器展示者的 [**IVMRSurfaceAllocator：： AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) 方法，以提供 VMR 的 [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) 介面指標。 配置器呈現者在使用 [**IVMRSurfaceAllocatorNotify：： NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) 方法將事件傳遞給 VMR 時，會使用這個介面指標。

作為替代方案，應用程式可以使用它自己的配置器展示者和預設配置器-展示者。 在此案例中，自訂配置器展示者只會處理需要自訂功能的呼叫，並將其餘的呼叫從 VMR 傳遞至預設配置器-展示者。 在許多情況下，只需要覆寫 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 介面。

![使用兩個配置器-展示者](images/custom-ap2.png)

若要同時使用自訂配置器提供者和預設配置器-展示者，應用程式會先呼叫 [**IVMRSurfaceAllocatorNotify：： AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) ，以提供指向新配置器的指標。 這會導致預設配置器-展示者終結，因此應用程式必須在 VMR 上呼叫 **QueryInterface** 並要求 [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) 介面，以建立另一個實例。 如上圖所示，自訂配置器呈現者會覆寫 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 介面方法，並只會將 **IVMRSurfaceAllocator** 介面的所有呼叫都傳遞至預設的實值。 此圖也會顯示在配置器上執行的 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[提供 VMR-9 的自訂 Allocator-Presenter](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[VMR Renderless 播放模式 (自訂配置器-展示者) ](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



