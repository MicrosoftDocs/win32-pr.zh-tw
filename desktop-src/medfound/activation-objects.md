---
description: 啟用物件
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: 啟用物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113440"
---
# <a name="activation-objects"></a><span data-ttu-id="1d4d1-103">啟用物件</span><span class="sxs-lookup"><span data-stu-id="1d4d1-103">Activation Objects</span></span>

<span data-ttu-id="1d4d1-104">*啟用物件* 是用來建立另一個物件的 helper 物件，與 class factory 有點類似。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-104">An *activation object* is a helper object that is used to create another object, somewhat similar to a class factory.</span></span> <span data-ttu-id="1d4d1-105">啟用物件會公開 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-105">Activation objects expose the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

<span data-ttu-id="1d4d1-106">啟始物件可讓您延遲建立目標物件，因為您可以在不建立目標物件的情況下，保留在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標上。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-106">An activation object lets you defer the creation of the target object, because you can hold onto an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer without creating the target object.</span></span> <span data-ttu-id="1d4d1-107">啟用物件也可以序列化，因此用來在另一個進程中建立目標物件。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-107">Activation objects can also be serialized, and thus used to create the target object in another process.</span></span> <span data-ttu-id="1d4d1-108">例如，啟用物件是用來將管線元件從應用程式程式封送處理到受保護的媒體路徑， (PMP) 進程。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-108">For example, activation objects are used to marshal pipeline components from the application process to the protected media path (PMP) process.</span></span> <span data-ttu-id="1d4d1-109">傳回 **IMFActivate** 指標清單的特定列舉函數也會使用啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-109">Activation objects are also used by certain enumeration functions that return a list of **IMFActivate** pointers.</span></span> <span data-ttu-id="1d4d1-110">在應用程式建立目標物件之前，它可以檢查啟用物件上的屬性，以取得物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-110">Before the application creates the target object, it can get information about the object by examining attributes on the activation object.</span></span>

<span data-ttu-id="1d4d1-111">若要從啟用物件建立目標物件，請呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-111">To create the target object from an activation object, call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method.</span></span> <span data-ttu-id="1d4d1-112">使用已建立的物件完成時，呼叫端必須呼叫 [**IMFActivate：： ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) 。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-112">The caller must call [**IMFActivate::ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) when it is done using the created object.</span></span> <span data-ttu-id="1d4d1-113">應用程式通常會建立啟用物件，而媒體會話會呼叫 **ActivateObject**。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-113">Often the application creates the activation object, and the Media Session calls **ActivateObject**.</span></span> <span data-ttu-id="1d4d1-114">在此情況下，媒體會話（而不是應用程式）必須呼叫 **ShutdownObject**。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-114">In that case, the Media Session, not the application, must call **ShutdownObject**.</span></span> <span data-ttu-id="1d4d1-115">在其他情況下，應用程式會接收來自媒體會話的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標，而應用程式會呼叫 **ActivateObject** 和 **ShutdownObject**。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-115">In other situations, the application receives an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer from the Media Session, and the application calls **ActivateObject** and **ShutdownObject**.</span></span> <span data-ttu-id="1d4d1-116"> (例如，請參閱 [如何播放受保護的媒體](how-to-play-protected-media-files.md)檔案。 ) </span><span class="sxs-lookup"><span data-stu-id="1d4d1-116">(For example, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).)</span></span>

<span data-ttu-id="1d4d1-117">啟用物件可以有屬性，而 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-117">Activation objects can have attributes, and the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="1d4d1-118">某些啟用物件會使用屬性來設定建立的物件。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-118">Some activation objects use attributes to configure the created object.</span></span> <span data-ttu-id="1d4d1-119">每個物件所支援的特定屬性都記載于該啟用物件建立函式的參考中。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-119">The specific attributes supported by each object are documented in the reference for that activation object's creation function.</span></span> <span data-ttu-id="1d4d1-120">使用您從函數接收的 **IMFActivate** 指標來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-120">Set the attributes using the **IMFActivate** pointer that you receive from the function.</span></span>

<span data-ttu-id="1d4d1-121">針對受保護的播放，啟始物件會封送處理至 PMP 程式。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-121">For protected playback, activation objects are marshaled to the PMP process.</span></span> <span data-ttu-id="1d4d1-122">若要支援封送處理，啟用物件必須公開 **IPersistStream** 介面。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-122">To support marshaling, an activation object must expose the **IPersistStream** interface.</span></span> <span data-ttu-id="1d4d1-123">此外，如果 PMP 是在受保護的進程中執行，則啟用物件和建立的物件都必須是信任的元件。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-123">In addition, both the activation object and the created object must be trusted components if the PMP is running in a protected process.</span></span> <span data-ttu-id="1d4d1-124">在未受保護的進程中載入 PMP 時，不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-124">This is not a requirement when the PMP is loaded in an unprotected process.</span></span>

<span data-ttu-id="1d4d1-125">若要在 PMP 程式中使用自訂管線物件 (例如媒體接收器) ，您必須為管線物件執行啟用物件：</span><span class="sxs-lookup"><span data-stu-id="1d4d1-125">To use a custom pipeline object (such as a media sink) inside the PMP process, you must implement an activation object for your pipeline object:</span></span>

-   <span data-ttu-id="1d4d1-126">啟用物件必須公開 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 和 **IPersistStream**。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-126">The activation object must expose [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) and **IPersistStream**.</span></span>
-   <span data-ttu-id="1d4d1-127">啟用物件的 **IPersist：： GetClassID** 方法必須傳回啟用物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-127">The activation object's **IPersist::GetClassID** method must return the activation object's CLSID.</span></span>
-   <span data-ttu-id="1d4d1-128">（選擇性）您可以執行 **IPersistStream：： Save** 和 **IPersistStream：： Load** 方法來封送處理您設定啟用物件所需的任何資料。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-128">Optionally, you can implement the **IPersistStream::Save** and **IPersistStream::Load** methods to marshal any data that you need to configure your activation object.</span></span>

<span data-ttu-id="1d4d1-129">當媒體會話在 PMP 程式中載入拓撲時，它會呼叫 **CoCreateInstance** 來建立新的啟用物件實例。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-129">When the Media Session loads the topology inside the PMP process, it calls **CoCreateInstance** to create a new instance of your activation object.</span></span> <span data-ttu-id="1d4d1-130">然後，它會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立管線物件。</span><span class="sxs-lookup"><span data-stu-id="1d4d1-130">Then it calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the pipeline object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d4d1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d4d1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d4d1-132">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="1d4d1-132">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="1d4d1-133">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="1d4d1-133">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



