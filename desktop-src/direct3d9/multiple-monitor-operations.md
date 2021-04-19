---
description: 成功重設裝置時 (IDirect3DDevice9：： Reset) 或在全螢幕操作中建立 (IDirect3D9：： CreateDevice) ，建立裝置的 Direct3D 物件會標示為擁有該系統上的所有介面卡。
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: 'Multiple-Monitor 作業 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998428"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="37937-103">Multiple-Monitor 作業 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="37937-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="37937-104">成功重設裝置時 ([**IDirect3DDevice9：： reset**](/windows/desktop/api)) 或在全螢幕操作中建立 ([**IDirect3D9：： CreateDevice**](/windows/desktop/api)) ，建立裝置的 Direct3D 物件會標示為擁有該系統上的所有介面卡。</span><span class="sxs-lookup"><span data-stu-id="37937-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="37937-105">此狀態稱為獨佔模式，且 Direct3D 物件擁有獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="37937-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="37937-106">獨佔模式表示任何其他 Direct3D 物件所建立的裝置都不能假設全螢幕作業，也不會配置視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="37937-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="37937-107">此外，當 Direct3D 物件採用獨佔模式時，所有未進入全螢幕的裝置都會處於遺失狀態。</span><span class="sxs-lookup"><span data-stu-id="37937-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="37937-108">如需詳細資訊，請參閱 [ (Direct3D 9) 的遺失裝置 ](lost-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="37937-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="37937-109">除了獨佔模式，Direct3D 物件也會收到裝置將使用之焦點視窗的通知。</span><span class="sxs-lookup"><span data-stu-id="37937-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="37937-110">當該 Direct3D 物件所擁有的最終全螢幕裝置重設為視窗模式或損毀時，就會釋放獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="37937-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="37937-111">當 Direct3D 物件擁有獨佔模式時，裝置可以分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="37937-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="37937-112">裝置的第一個類別具有下列特性。</span><span class="sxs-lookup"><span data-stu-id="37937-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="37937-113">它們是由建立全螢幕裝置的相同 Direct3D 物件所建立。</span><span class="sxs-lookup"><span data-stu-id="37937-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="37937-114">它們與全螢幕裝置具有相同的焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="37937-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="37937-115">它們代表與任何全螢幕裝置不同的介面卡。</span><span class="sxs-lookup"><span data-stu-id="37937-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="37937-116">此類別中的裝置對於其重設或建立的能力沒有任何限制，且未處於遺失狀態。</span><span class="sxs-lookup"><span data-stu-id="37937-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="37937-117">此類別中的裝置甚至可以放入全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="37937-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="37937-118">不屬於第一個類別目錄的裝置-由另一個 Direct3D 物件建立的裝置、使用不同的焦點視窗建立，以及針對裝置已全螢幕的介面卡建立的裝置，在獨佔模式遺失之前，無法重設並維持遺失狀態。</span><span class="sxs-lookup"><span data-stu-id="37937-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="37937-119">如此一來，多監視器應用程式就可以在全螢幕模式下放置數部裝置，但只有當這些裝置適用于不同的介面卡時，才會由相同的 Direct3D 物件建立，並共用相同的焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="37937-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37937-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="37937-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37937-121">呈現場景</span><span class="sxs-lookup"><span data-stu-id="37937-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



