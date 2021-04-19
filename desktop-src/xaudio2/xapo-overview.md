---
description: XAPO API 可讓您建立跨平臺音訊處理物件 (XAPO) ，以在 Windows 和 Xbox 360 的 XAudio2 中使用。
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: XAPO 概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975327"
---
# <a name="xapo-overview"></a><span data-ttu-id="6b15b-103">XAPO 概觀</span><span class="sxs-lookup"><span data-stu-id="6b15b-103">XAPO Overview</span></span>

<span data-ttu-id="6b15b-104">XAPO API 可讓您建立跨平臺音訊處理物件 (XAPO) ，以在 Windows 和 Xbox 360 的 XAudio2 中使用。</span><span class="sxs-lookup"><span data-stu-id="6b15b-104">The XAPO API allows the creation of cross-platform audio processing objects (XAPO) for use in XAudio2 on both Windows and Xbox 360.</span></span> <span data-ttu-id="6b15b-105">XAPO 是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。</span><span class="sxs-lookup"><span data-stu-id="6b15b-105">An XAPO is an object that takes incoming audio data, and performs some operation on the data before passing it on.</span></span> <span data-ttu-id="6b15b-106">您可以使用 XAPO 來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。</span><span class="sxs-lookup"><span data-stu-id="6b15b-106">You can use an XAPO to perform a variety of tasks, including adding reverb to an audio stream and monitoring peak volume levels.</span></span>

## <a name="creating-new-xapos"></a><span data-ttu-id="6b15b-107">建立新的 XAPOs</span><span class="sxs-lookup"><span data-stu-id="6b15b-107">Creating New XAPOs</span></span>

<span data-ttu-id="6b15b-108">XAPO API 會提供 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 類別來建立新的 XAPO 類型。</span><span class="sxs-lookup"><span data-stu-id="6b15b-108">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="6b15b-109">**IXAPO** 介面包含所有需要實作為建立新 XAPO 的方法。</span><span class="sxs-lookup"><span data-stu-id="6b15b-109">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="6b15b-110">**CXAPOBase** 類別提供 **IXAPO** 介面的基本實作為。</span><span class="sxs-lookup"><span data-stu-id="6b15b-110">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="6b15b-111">**CXAPOBase** 會執行所有 **IXAPO** 介面方法，但是 [**IXAPO：:P ROCESS**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法是每個 XAPO 唯一的。</span><span class="sxs-lookup"><span data-stu-id="6b15b-111">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

<span data-ttu-id="6b15b-112">如需建立新 XAPO 的範例，請參閱 [如何：建立 XAPO](how-to--create-an-xapo.md)。</span><span class="sxs-lookup"><span data-stu-id="6b15b-112">For an example of creating a new XAPO, see [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

<span data-ttu-id="6b15b-113">如需建立接受執行時間參數之 XAPO 的範例，請參閱 [如何：將執行時間參數支援加入至 XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md)。</span><span class="sxs-lookup"><span data-stu-id="6b15b-113">For an example of creating a XAPO that accepts run-time parameters, see [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

## <a name="xapos-and-com"></a><span data-ttu-id="6b15b-114">XAPOs 和 COM</span><span class="sxs-lookup"><span data-stu-id="6b15b-114">XAPOs and COM</span></span>

<span data-ttu-id="6b15b-115">XAPOs 會執行 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="6b15b-115">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="6b15b-116">[**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)和 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)介面包括三個 **IUnknown** 方法： **QueryInterface**、 **AddRef** 和 **Release**。</span><span class="sxs-lookup"><span data-stu-id="6b15b-116">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="6b15b-117">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 提供這三種 IUnknown 方法的所有方法。</span><span class="sxs-lookup"><span data-stu-id="6b15b-117">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the IUnknown methods.</span></span> <span data-ttu-id="6b15b-118">**CXAPOBase** 的新實例會有1的參考計數。</span><span class="sxs-lookup"><span data-stu-id="6b15b-118">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="6b15b-119">當其參考計數變成0時，就會將它終結。</span><span class="sxs-lookup"><span data-stu-id="6b15b-119">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="6b15b-120">**IXAPO** 和 **IXAPOParameters** 的執行應該遵循相同的模式，以便在與 XAudio2 搭配使用時，能夠適當地進行管理。</span><span class="sxs-lookup"><span data-stu-id="6b15b-120">Implementations of **IXAPO** and **IXAPOParameters** should follow the same pattern to allow for their proper management when used with XAudio2.</span></span>

<span data-ttu-id="6b15b-121">XAPO 實例會以 **IUnknown** 介面的形式傳遞至 XAudio2。</span><span class="sxs-lookup"><span data-stu-id="6b15b-121">XAPO instances are passed to XAudio2 as **IUnknown** interfaces.</span></span> <span data-ttu-id="6b15b-122">XAudio2 會使用 **QueryInterface** 來取得 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面，以及偵測 XAPO 是否會實作為 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) 介面。</span><span class="sxs-lookup"><span data-stu-id="6b15b-122">XAudio2 uses **QueryInterface** to acquire an [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and to detect whether the XAPO implements the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="6b15b-123">**IXAPO** 的執行必須接受 **\_ \_ uuidof (IXAPO)** 的要求。</span><span class="sxs-lookup"><span data-stu-id="6b15b-123">Implementations of **IXAPO** must accept requests for **\_\_uuidof(IXAPO)**.</span></span> <span data-ttu-id="6b15b-124">如果 **IXAPOParameters** 已實作為，它也必須接受 **\_ \_ uuidof (IXAPOParameters)** 的要求。</span><span class="sxs-lookup"><span data-stu-id="6b15b-124">If **IXAPOParameters** is implemented, it must also accept requests for **\_\_uuidof(IXAPOParameters)**.</span></span>

## <a name="using-an-xapo-in-xaudio2"></a><span data-ttu-id="6b15b-125">在 XAudio2 中使用 XAPO</span><span class="sxs-lookup"><span data-stu-id="6b15b-125">Using an XAPO in XAudio2</span></span>

<span data-ttu-id="6b15b-126">XAPOs 會在 XAudio2 中使用，方法是將它們附加至語音。</span><span class="sxs-lookup"><span data-stu-id="6b15b-126">XAPOs are used in XAudio2 by attaching them to voices.</span></span> <span data-ttu-id="6b15b-127">每個 XAudio2 voice 都有一個效果鏈，其中包含零或多個音訊效果。</span><span class="sxs-lookup"><span data-stu-id="6b15b-127">Each XAudio2 voice has an effect chain containing zero or more audio effects.</span></span> <span data-ttu-id="6b15b-128">傳送至語音的音訊資料會在傳送到語音輸出目標之前通過鏈中的每個效果。</span><span class="sxs-lookup"><span data-stu-id="6b15b-128">Audio data sent to a voice is passed through each effect in the chain before it is sent to the voice's output targets.</span></span> <span data-ttu-id="6b15b-129">使用 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)方法的 *pInputProcessParameters* 參數，將資料從語音傳遞到每個效果。</span><span class="sxs-lookup"><span data-stu-id="6b15b-129">Data is passed from the voice to each effect using the *pInputProcessParameters* parameter of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span> <span data-ttu-id="6b15b-130">然後使用 *pOutputProcessParameters* 參數將它傳回給語音。</span><span class="sxs-lookup"><span data-stu-id="6b15b-130">Then it is returned to the voice using the *pOutputProcessParameters* parameter.</span></span> <span data-ttu-id="6b15b-131">語音會取得每個效果的輸出，然後將其送入鏈中的下一個效果，直到鏈中沒有任何效果。</span><span class="sxs-lookup"><span data-stu-id="6b15b-131">The voice takes the output of each effect, and feeds it into the next effect in the chain until no effects are left in the chain.</span></span>

<span data-ttu-id="6b15b-132">如需 XAudio2 效果鏈的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md)。</span><span class="sxs-lookup"><span data-stu-id="6b15b-132">For more information about XAudio2 effect chains, see [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>

<span data-ttu-id="6b15b-133">如需在 XAudio2 中使用 XAPO 的範例，請參閱 how [to：使用 XAudio2 中的 XAPO](how-to--use-an-xapo-in-xaudio2.md)。</span><span class="sxs-lookup"><span data-stu-id="6b15b-133">For an example of using an XAPO in XAudio2, see [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md).</span></span>

## <a name="effect-libraries"></a><span data-ttu-id="6b15b-134">效果程式庫</span><span class="sxs-lookup"><span data-stu-id="6b15b-134">Effect Libraries</span></span>

<span data-ttu-id="6b15b-135">XAPO 效果程式庫包含數個 XAPOs，以及用來具現化它們的常用方法。</span><span class="sxs-lookup"><span data-stu-id="6b15b-135">The XAPO effect library contains several XAPOs, and a common method of instantiating them.</span></span> <span data-ttu-id="6b15b-136">如需 XAPOFX 的詳細資訊，請參閱 [XAPOFX 總覽](xapofx-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="6b15b-136">See [XAPOFX Overview](xapofx-overview.md) for information about XAPOFX.</span></span> <span data-ttu-id="6b15b-137">此外，XAudio2 也有內建的「回音」和「大量計量」效果。</span><span class="sxs-lookup"><span data-stu-id="6b15b-137">Also, XAudio2 has built-in reverb and volume meter effects.</span></span> <span data-ttu-id="6b15b-138">如需內建 XAudio2 效果的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) 。</span><span class="sxs-lookup"><span data-stu-id="6b15b-138">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for more information about the built-in XAudio2 effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b15b-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b15b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b15b-140">音訊效果</span><span class="sxs-lookup"><span data-stu-id="6b15b-140">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="6b15b-141">XAudio2 音訊效果</span><span class="sxs-lookup"><span data-stu-id="6b15b-141">XAudio2 Audio Effects</span></span>](xaudio2-audio-effects.md)
</dt> </dl>

 

 
