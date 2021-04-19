---
description: 本節說明 IMM 介面。
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: 輸入方法管理員介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997533"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="401cf-103">輸入方法管理員介面</span><span class="sxs-lookup"><span data-stu-id="401cf-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="401cf-104">本節說明 IMM 介面。</span><span class="sxs-lookup"><span data-stu-id="401cf-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="401cf-105">介面</span><span class="sxs-lookup"><span data-stu-id="401cf-105">Interface</span></span>                                                            | <span data-ttu-id="401cf-106">描述</span><span class="sxs-lookup"><span data-stu-id="401cf-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="401cf-107">**IFECommon**</span><span class="sxs-lookup"><span data-stu-id="401cf-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="401cf-108">提供不同語言通用的 IME 相關服務。</span><span class="sxs-lookup"><span data-stu-id="401cf-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="401cf-109">**IFEDictionary**</span><span class="sxs-lookup"><span data-stu-id="401cf-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="401cf-110">允許用戶端存取 Microsoft IME 使用者字典。</span><span class="sxs-lookup"><span data-stu-id="401cf-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="401cf-111">**IFELanguage**</span><span class="sxs-lookup"><span data-stu-id="401cf-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="401cf-112">使用 Microsoft IME 提供語言處理服務。</span><span class="sxs-lookup"><span data-stu-id="401cf-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="401cf-113">**IImePad**</span><span class="sxs-lookup"><span data-stu-id="401cf-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="401cf-114">從 IMEPadApplets 執行 [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) 介面的應用程式中插入文字。</span><span class="sxs-lookup"><span data-stu-id="401cf-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="401cf-115">**IImePadApplet**</span><span class="sxs-lookup"><span data-stu-id="401cf-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="401cf-116">透過 [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) 介面將字串輸入應用程式。</span><span class="sxs-lookup"><span data-stu-id="401cf-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="401cf-117">**IImePlugInDictDictionaryList**</span><span class="sxs-lookup"><span data-stu-id="401cf-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="401cf-118">提供對 IME 外掛程式字典清單的存取權。</span><span class="sxs-lookup"><span data-stu-id="401cf-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="401cf-119">**IImeSpecifyApplets**</span><span class="sxs-lookup"><span data-stu-id="401cf-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="401cf-120">指定從 [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) 介面物件呼叫的方法，以模擬 [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) 介面。</span><span class="sxs-lookup"><span data-stu-id="401cf-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



