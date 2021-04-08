---
description: Stream 控制項
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Stream 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850359"
---
# <a name="stream-control"></a><span data-ttu-id="1793b-103">Stream 控制項</span><span class="sxs-lookup"><span data-stu-id="1793b-103">Stream Control</span></span>

<span data-ttu-id="1793b-104">VMR 的輸入 pin () s 的 [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) 介面，可讓應用程式和上游篩選器控制混音器元件的行為，包括 Z 順序和 VMR 輸入資料流程的作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="1793b-104">The [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) interface on the VMR's input pin(s) enables applications and upstream filters to control the behavior of the mixer component, including the Z-order and the active state of the VMR's input streams.</span></span> <span data-ttu-id="1793b-105">雖然此介面是在針腳上公開，但它會在 VMR 的混音器元件上運作，因此只有在載入混音器時才可使用，這是當 VMR 處理多個輸入資料流程時。</span><span class="sxs-lookup"><span data-stu-id="1793b-105">Although this interface is exposed on the pins, it operates on the VMR's mixer component, so it is only available when the mixer is loaded, which is when the VMR is processing multiple input streams.</span></span> <span data-ttu-id="1793b-106">上游篩選器會使用 [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) 和 [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) 方法來控制來源色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1793b-106">Upstream filters use the [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) and [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) methods to control the source color key.</span></span> <span data-ttu-id="1793b-107">這些方法會啟用像是動畫在影片上重迭的效果。</span><span class="sxs-lookup"><span data-stu-id="1793b-107">These methods enable effects such as the overlay of animation over video.</span></span> <span data-ttu-id="1793b-108">只要將色彩索引鍵設定為動畫資料流程的背景色彩，VMR 就會將該資料流程與另一個影片資料流程混合。</span><span class="sxs-lookup"><span data-stu-id="1793b-108">Simply set the color key to the animation stream's background color, and the VMR will mix that stream with another video stream.</span></span> <span data-ttu-id="1793b-109">應用程式應該小心不要將色彩索引鍵變更為與上游篩選器所使用的值不同的值，例如解碼器。</span><span class="sxs-lookup"><span data-stu-id="1793b-109">Applications should take care not to change the color key to some value that is different than the value being used by an upstream filter, such as a decoder.</span></span>

<span data-ttu-id="1793b-110">篩選器會使用 [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) 和 [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) 方法，告知混音器是否預期輸入來自指定 pin 的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="1793b-110">Filters use the [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) and [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) methods to tell the mixer whether to expect input data from a specified pin.</span></span> <span data-ttu-id="1793b-111">例如，Line21 解碼器只會在資料流程中有該資料時，使用這些方法來啟用 Line21 資料的 VMR 輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="1793b-111">For example, the Line21 Decoder uses these methods to activate the VMR's input pin for Line21 data only when that data is present in the stream.</span></span> <span data-ttu-id="1793b-112">將 pin 設定為非作用中狀態，會指示混音器不要等待指定 pin 的資料，然後再組合影像。</span><span class="sxs-lookup"><span data-stu-id="1793b-112">Setting a pin to an inactive state instructs the mixer not to wait for data from a specified pin before compositing the image.</span></span>

 

 



