---
title: '文字服務架構 (文字服務架構) '
description: Microsoft Windows 文字服務架構 (TSF) 是一種系統服務，可作為 Windows 2000 的可轉散發套件。
ms.assetid: ecc34b2e-89e8-48a8-8a8e-442d2145fe24
ms.topic: article
ms.date: 01/14/2020
ms.openlocfilehash: 9c21cae442b5fbed62c00010a17849d1d5f27b49
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685380"
---
# <a name="text-services-framework-text-services-framework"></a><span data-ttu-id="8c6b0-103">文字服務架構 (文字服務架構) </span><span class="sxs-lookup"><span data-stu-id="8c6b0-103">Text Services Framework (Text Services Framework)</span></span>

## <a name="purpose"></a><span data-ttu-id="8c6b0-104">目的</span><span class="sxs-lookup"><span data-stu-id="8c6b0-104">Purpose</span></span>

<span data-ttu-id="8c6b0-105">Microsoft Windows 文字服務架構 (TSF) 是一種系統服務，可作為 Windows 的可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-105">Microsoft Windows Text Services Framework (TSF) is a system service available as a redistributable for Windows.</span></span> <span data-ttu-id="8c6b0-106">TSF 提供簡單且可擴充的架構，可提供先進的文字輸入和自然語言技術。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-106">TSF provides a simple and scalable framework for the delivery of advanced text input and natural language technologies.</span></span> <span data-ttu-id="8c6b0-107">TSF 可在應用程式中啟用，也可以在 TSF 文字服務中啟用。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-107">TSF can be enabled in applications, or as a TSF text service.</span></span> <span data-ttu-id="8c6b0-108">TSF 文字服務可提供多語系支援並傳遞文字服務，例如鍵盤處理器、手寫辨識和語音辨識。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-108">A TSF text service provides multilingual support and delivers text services such as keyboard processors, handwriting recognition, and speech recognition.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8c6b0-109">適用時</span><span class="sxs-lookup"><span data-stu-id="8c6b0-109">Where applicable</span></span>

<span data-ttu-id="8c6b0-110">文字服務架構適用于使用文字服務和 Windows XP 或更新版本作業系統的 Windows 電腦。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-110">Text Services Framework is applicable for Windows-based computers using text services and Windows XP or later versions of the operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8c6b0-111">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8c6b0-111">Developer audience</span></span>

<span data-ttu-id="8c6b0-112">文字服務架構的設計目的是要讓元件物件模型使用 C/c + + 程式設計語言 (COM) 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-112">Text Services Framework is designed for use by Component Object Model (COM) programmers using the C/C++ programming languages.</span></span> <span data-ttu-id="8c6b0-113">程式設計人員應該熟悉 Windows 電腦的文字服務。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-113">Programmers should be familiar with text services for Windows-based computers.</span></span> <span data-ttu-id="8c6b0-114">建議您瞭解手寫辨識、語音辨識，以及多語系支援的程式設計。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-114">Knowledge of handwriting recognition, speech recognition, and programming for multilingual support is recommended.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8c6b0-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8c6b0-115">Run-time requirements</span></span>

<span data-ttu-id="8c6b0-116">如需最新的可轉散發套件，請下載 [Windows 10 PLATFORM SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-116">For the latest redistributable, download the [Windows 10 platform SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="8c6b0-117">如需特定 API 元素需求的詳細資訊，請參閱 < (/windows/win32/tsf/text-services-framework-reference) [TFS 參考檔] 中的需求一節。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-117">For more information about the requirements of specific API elements, see the Requirements section in the ](/windows/win32/tsf/text-services-framework-reference)[TFS reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8c6b0-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="8c6b0-118">In this section</span></span>



| <span data-ttu-id="8c6b0-119">主題</span><span class="sxs-lookup"><span data-stu-id="8c6b0-119">Topic</span></span>                                                                                 | <span data-ttu-id="8c6b0-120">描述</span><span class="sxs-lookup"><span data-stu-id="8c6b0-120">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c6b0-121">關於文字服務架構</span><span class="sxs-lookup"><span data-stu-id="8c6b0-121">About Text Services Framework</span></span>](about-text-services-framework.md)<br/>         | <span data-ttu-id="8c6b0-122">文字服務架構的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-122">General information about Text Services Framework.</span></span><br/>                                                    |
| [<span data-ttu-id="8c6b0-123">使用文字服務架構</span><span class="sxs-lookup"><span data-stu-id="8c6b0-123">Using Text Services Framework</span></span>](using-text-services-framework.md)<br/>         | <span data-ttu-id="8c6b0-124">使用文字服務架構的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-124">Information about using Text Services Framework.</span></span><br/>                                                      |
| [<span data-ttu-id="8c6b0-125">文字服務架構參考</span><span class="sxs-lookup"><span data-stu-id="8c6b0-125">Text Services Framework Reference</span></span>](text-services-framework-reference.md)<br/> | <span data-ttu-id="8c6b0-126">文字服務架構介面、方法、結構和其他程式碼元素的相關檔。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-126">Documentation about Text Services Framework interfaces, methods, structures, and other code elements.</span></span><br/> |
| [<span data-ttu-id="8c6b0-127">詞彙</span><span class="sxs-lookup"><span data-stu-id="8c6b0-127">Glossary</span></span>](glossary.md)<br/>                                                   | <span data-ttu-id="8c6b0-128">本檔中所使用的技術詞彙清單（依字母順序排列）。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-128">Alphabetical listing of technical terms used in this documentation.</span></span><br/>                                   |



 

## <a name="additional-resources"></a><span data-ttu-id="8c6b0-129">其他資源</span><span class="sxs-lookup"><span data-stu-id="8c6b0-129">Additional resources</span></span>

<span data-ttu-id="8c6b0-130">閱讀本指南之前，您應該知道的事項</span><span class="sxs-lookup"><span data-stu-id="8c6b0-130">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="8c6b0-131">基於文字服務架構說明的目的，「應用程式」一詞是指已啟用 TSF 的應用程式，「文字服務」一詞指的是 TSF 文字服務，「經理」一詞指的是 TSF 管理員。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-131">For the purposes of the Text Services Framework Help, the term "application" refers to a TSF-enabled application, the term "text service" refers to a TSF text service, and the term "manager" refers to the TSF manager.</span></span> <span data-ttu-id="8c6b0-132">除非另有指定，否則每個詞彙都適用于此處所述。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-132">Each term applies as stated herein unless otherwise specified.</span></span> <span data-ttu-id="8c6b0-133">文字服務提供者應該提供數位簽章給其二進位可執行檔。</span><span class="sxs-lookup"><span data-stu-id="8c6b0-133">Text service providers should provide digital signatures with their binary executables.</span></span>

 

 





