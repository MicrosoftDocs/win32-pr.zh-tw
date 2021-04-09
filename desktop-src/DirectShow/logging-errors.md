---
description: 記錄錯誤
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: 記錄錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687663"
---
# <a name="logging-errors"></a><span data-ttu-id="14c45-103">記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="14c45-103">Logging Errors</span></span>

<span data-ttu-id="14c45-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="14c45-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="14c45-105"> (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)提供內建機制，可記錄載入、建立或轉譯 DES 專案時所發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="14c45-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="14c45-106">本文提供範例主控台應用程式，此應用程式會載入 XML 專案檔，並嘗試加以呈現。</span><span class="sxs-lookup"><span data-stu-id="14c45-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="14c45-107">如果發生錯誤，應用程式會在主控台視窗中列印錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="14c45-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="14c45-108">本文所提供的範例程式碼是以 [載入和預覽專案](loading-and-previewing-a-project.md)時所提供的範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="14c45-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="14c45-109">您的應用程式不需要執行錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="14c45-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="14c45-110">除非您明確要求，否則 DES 不會記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="14c45-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="14c45-111">本文假設您瞭解 COM 用戶端程式設計和 DES 時間軸模型。</span><span class="sxs-lookup"><span data-stu-id="14c45-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="14c45-112">此外，您還需要瞭解 COM 物件程式設計的基本概念。</span><span class="sxs-lookup"><span data-stu-id="14c45-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="14c45-113">如需 DES 中時間軸的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。</span><span class="sxs-lookup"><span data-stu-id="14c45-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="14c45-114">本文包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="14c45-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="14c45-115">錯誤記錄總覽</span><span class="sxs-lookup"><span data-stu-id="14c45-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="14c45-116">建立錯誤記錄類別</span><span class="sxs-lookup"><span data-stu-id="14c45-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="14c45-117">執行 IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="14c45-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="14c45-118">設定錯誤記錄檔</span><span class="sxs-lookup"><span data-stu-id="14c45-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="14c45-119">DES 錯誤記錄：範例程式碼</span><span class="sxs-lookup"><span data-stu-id="14c45-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="14c45-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="14c45-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14c45-121">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="14c45-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



