---
description: 使用手勢的總覽。
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: 使用手勢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943395"
---
# <a name="using-gestures"></a><span data-ttu-id="12e5b-103">使用手勢</span><span class="sxs-lookup"><span data-stu-id="12e5b-103">Using Gestures</span></span>

<span data-ttu-id="12e5b-104">Tablet PC 平臺提供 Microsoft 手勢辨識器，可支援應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="12e5b-105">如需 Microsoft 手勢辨識器所支援的手勢清單，請參閱 [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉中的應用程式手勢表格。</span><span class="sxs-lookup"><span data-stu-id="12e5b-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="12e5b-106">Tablet PC 也支援系統手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="12e5b-107">如需 Tablet PC 支援的系統筆勢清單，請參閱 [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) 列舉中的系統手勢表格。</span><span class="sxs-lookup"><span data-stu-id="12e5b-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="12e5b-108">Microsoft 手勢辨識器</span><span class="sxs-lookup"><span data-stu-id="12e5b-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="12e5b-109">您可以使用 [**InkCollector**](inkcollector-class.md)物件的 [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)屬性、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項來採用 Microsoft 手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="12e5b-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="12e5b-110">將 **CollectionMode** 屬性設定為混合模式 (**InkAndGesture**) 或僅限手勢模式 (**GestureOnly**) 預設會將筆墨傳遞給 Microsoft 手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="12e5b-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="12e5b-111">您可以將 [ [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) ] 屬性設定為 [ **InkAndGesture**]，以搭配 [InkEdit](inkedit-control-reference.md)控制項來使用 Microsoft 手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="12e5b-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="12e5b-112">您也可以藉由將 [**GestureRecognizer**](gesturerecognizer-class.md)物件新增至其中一個外掛程式集合，來搭配使用手勢辨識和 [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)物件。</span><span class="sxs-lookup"><span data-stu-id="12e5b-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="12e5b-113">但是，如果目前的 Microsoft 手勢辨識器版本不支援您想要使用的手勢，您可以建立自己的辨識器，並將它與 Microsoft 手勢辨識器搭配使用。</span><span class="sxs-lookup"><span data-stu-id="12e5b-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="12e5b-114">這可讓您在應用程式中完整支援筆勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="12e5b-115">Tablet PC 針對部分或所有輸入使用畫筆。</span><span class="sxs-lookup"><span data-stu-id="12e5b-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="12e5b-116">這可讓您輕鬆地撰寫筆跡。</span><span class="sxs-lookup"><span data-stu-id="12e5b-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="12e5b-117">Tablet PC 平臺提供可支援各項手勢分層結構的手寫筆輸入架構。</span><span class="sxs-lookup"><span data-stu-id="12e5b-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="12e5b-118">您可以定義手勢和對應，讓使用者在新的表面上撰寫和叫用先進的手勢，同時保留可叫用其他 Windows 架構應用程式之傳統滑鼠訊息的手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="12e5b-119">Tablet PC 平臺導入了兩個層級的手勢：系統手勢，也稱為系統事件和應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="12e5b-120">畫筆架構支援系統和應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="12e5b-121">支援單筆觸和多筆觸應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="12e5b-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12e5b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="12e5b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e5b-123">應用程式手勢</span><span class="sxs-lookup"><span data-stu-id="12e5b-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="12e5b-124">筆觸手勢</span><span class="sxs-lookup"><span data-stu-id="12e5b-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="12e5b-125">系統手勢</span><span class="sxs-lookup"><span data-stu-id="12e5b-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



