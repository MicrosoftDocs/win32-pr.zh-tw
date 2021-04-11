---
description: Winternl .h 標頭檔會公開內部 Windows Api 的原型。 沒有相關聯的匯入程式庫，因此開發人員必須使用執行時間動態連結來呼叫此標頭檔中所述的函式。
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: 呼叫內部 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936238"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="d75b4-104">呼叫內部 Api</span><span class="sxs-lookup"><span data-stu-id="d75b4-104">Calling Internal APIs</span></span>

<span data-ttu-id="d75b4-105">Winternl .h 標頭檔會公開內部 Windows Api 的原型。</span><span class="sxs-lookup"><span data-stu-id="d75b4-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="d75b4-106">沒有相關聯的匯入程式庫，因此開發人員必須使用執行時間動態連結來呼叫此標頭檔中所述的函式。</span><span class="sxs-lookup"><span data-stu-id="d75b4-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="d75b4-107">Winternl 中的函式和結構是作業系統內部的函式和結構，而且可能會從某個 Windows 版本變更為下一個版本，而且可能甚至是每個版本的 service pack 之間的變更。</span><span class="sxs-lookup"><span data-stu-id="d75b4-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="d75b4-108">為了維持應用程式的相容性，您應該改為使用對等的公用函數。</span><span class="sxs-lookup"><span data-stu-id="d75b4-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="d75b4-109">您可以在標頭檔、Winternl 和每個函式的檔中找到進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="d75b4-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="d75b4-110">如果您使用這些函式，您可以透過使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)的執行時間動態連結來存取這些函數。</span><span class="sxs-lookup"><span data-stu-id="d75b4-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="d75b4-111">這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。</span><span class="sxs-lookup"><span data-stu-id="d75b4-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="d75b4-112">不過，簽章變更可能無法偵測。</span><span class="sxs-lookup"><span data-stu-id="d75b4-112">Signature changes, however, may not be detectable.</span></span>

 

 
