---
description: 專屬全螢幕模式的概念會保留在 Direct3D 9 中，但會在 IDirect3D9：： CreateDevice 和 IDirect3DDevice9：： Reset 方法呼叫中完全保持隱含。
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: '使用多個監視器系統 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972927"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a><span data-ttu-id="a991d-103">使用多個監視器系統 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a991d-103">Working with Multiple Monitor Systems (Direct3D 9)</span></span>

<span data-ttu-id="a991d-104">專屬全螢幕模式的概念會保留在 Direct3D 9 中，但會在 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 和 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 方法呼叫中完全保持隱含。</span><span class="sxs-lookup"><span data-stu-id="a991d-104">The concept of exclusive full-screen mode is retained in Direct3D 9, but it is kept entirely implicit in the [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) method calls.</span></span> <span data-ttu-id="a991d-105">每次成功重設或以全螢幕操作建立裝置時，建立裝置的 Direct3D 物件都會標示為擁有該系統上的所有介面卡。</span><span class="sxs-lookup"><span data-stu-id="a991d-105">Whenever a device is successfully reset or created in full-screen operation, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="a991d-106">此狀態稱為獨佔模式，而在此階段，Direct3D 物件會擁有獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="a991d-106">This state is known as exclusive mode, and at this point the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="a991d-107">獨佔模式表示任何其他 Direct3D9 物件所建立的裝置都不能假設全螢幕操作，也不會配置視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="a991d-107">Exclusive mode means that devices created by any other Direct3D9 object can neither assume full-screen operation nor allocate video memory.</span></span> <span data-ttu-id="a991d-108">此外，當 Direct3D9 物件採用獨佔模式時，全螢幕裝置以外的所有裝置都會進入遺失狀態。</span><span class="sxs-lookup"><span data-stu-id="a991d-108">In addition, when a Direct3D9 object assumes exclusive mode, all devices other than the device that went full-screen are placed into the lost state.</span></span> <span data-ttu-id="a991d-109">如需如何處理遺失裝置的詳細資訊，請參閱 [ (Direct3D 9) 的裝置遺失 ](lost-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="a991d-109">For information about how to handle lost devices, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="a991d-110">除了獨佔模式之外，Direct3D9 物件也會收到裝置所要使用之焦點視窗的通知。</span><span class="sxs-lookup"><span data-stu-id="a991d-110">Along with exclusive mode, the Direct3D9 object is informed of the focus window to be used by the device.</span></span> <span data-ttu-id="a991d-111">當該 Direct3D9 物件所擁有的最後全螢幕裝置重設為視窗模式或損毀時，就會釋放獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="a991d-111">Exclusive mode is released when the last full-screen device owned by that Direct3D9 object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="a991d-112">當 Direct3D9 物件擁有獨佔模式時，裝置可以分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="a991d-112">Devices can be divided into two categories when a Direct3D9 object owns exclusive mode.</span></span> <span data-ttu-id="a991d-113">裝置的第一個類別是由建立裝置已全螢幕的相同 Direct3D9 物件所建立的類別，與已經全螢幕的裝置具有相同的焦點視窗，並且代表任何全螢幕裝置的不同介面卡。</span><span class="sxs-lookup"><span data-stu-id="a991d-113">The first category of devices are those that were created by the same Direct3D9 object that created the device that is already full-screen, have the same focus window as the device that is already full-screen, and represent a different adapter from any full-screen device.</span></span> <span data-ttu-id="a991d-114">此類別中的裝置對於其重設或建立的能力沒有任何限制，且不會置於遺失狀態。</span><span class="sxs-lookup"><span data-stu-id="a991d-114">Devices in this category have no restrictions concerning their ability to be reset or created and are not placed into the lost state.</span></span> <span data-ttu-id="a991d-115">此類別中的裝置甚至可以放入全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="a991d-115">Devices in this category can even be placed into full-screen mode.</span></span>

<span data-ttu-id="a991d-116">不在此類別中的裝置，也就是由不同 Direct3D9 物件建立的裝置，或具有不同焦點視窗的裝置，或具有裝置已滿全螢幕的某些介面卡，無法重設並保持在遺失狀態，直到獨佔模式遺失為止。</span><span class="sxs-lookup"><span data-stu-id="a991d-116">Devices not in this category, which would be those created by a different Direct3D9 object, or with a different focus window, or for some adapter with a device already full-screen cannot be reset and remain in the lost state until exclusive mode is lost.</span></span>

<span data-ttu-id="a991d-117">實際的含意是，多個監視器應用程式可以將數個裝置放在全螢幕模式中，但只有當這些裝置適用于不同的介面卡時，才會由相同的 Direct3D9 物件建立，且全都共用相同的焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="a991d-117">The practical implication is that a multiple monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D9 object, and all share the same focus window.</span></span>

<span data-ttu-id="a991d-118">當您使用相同的 [**IDirect3D9**](/windows/desktop/api) 物件和焦點視窗來建立新裝置時，您的原始裝置將會遺失其表面。</span><span class="sxs-lookup"><span data-stu-id="a991d-118">When you create a new device using the same [**IDirect3D9**](/windows/desktop/api) object and focus window, your original device will lose its surfaces.</span></span> <span data-ttu-id="a991d-119">您必須在第一個裝置上呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ，才能讓您的應用程式使用它。</span><span class="sxs-lookup"><span data-stu-id="a991d-119">You will need to call [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) on the first device in order for your application to use it.</span></span> <span data-ttu-id="a991d-120">例如，若要建立兩個裝置，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a991d-120">For example, to create two devices, do the following:</span></span>

1.  <span data-ttu-id="a991d-121">建立裝置1</span><span class="sxs-lookup"><span data-stu-id="a991d-121">Create Device 1</span></span>
2.  <span data-ttu-id="a991d-122">建立裝置2</span><span class="sxs-lookup"><span data-stu-id="a991d-122">Create Device 2</span></span>
3.  <span data-ttu-id="a991d-123">重設裝置1</span><span class="sxs-lookup"><span data-stu-id="a991d-123">Reset Device 1</span></span>

## <a name="related-topics"></a><span data-ttu-id="a991d-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="a991d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a991d-125">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="a991d-125">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
