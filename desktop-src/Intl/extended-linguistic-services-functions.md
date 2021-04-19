---
description: ELS 支援下表中定義的函數。
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: 擴充的語言服務函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985196"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="bfc36-103">擴充的語言服務函數</span><span class="sxs-lookup"><span data-stu-id="bfc36-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="bfc36-104">ELS 支援下表中定義的函數。</span><span class="sxs-lookup"><span data-stu-id="bfc36-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="bfc36-105">函式</span><span class="sxs-lookup"><span data-stu-id="bfc36-105">Function</span></span>                                                 | <span data-ttu-id="bfc36-106">描述</span><span class="sxs-lookup"><span data-stu-id="bfc36-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfc36-107">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="bfc36-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="bfc36-108">應用程式定義的回呼函式，會以非同步方式處理 **MappingRecognizeText** 函數所產生的資料。</span><span class="sxs-lookup"><span data-stu-id="bfc36-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="bfc36-109">**MappingDoAction**</span><span class="sxs-lookup"><span data-stu-id="bfc36-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="bfc36-110">導致 ELS 服務在文字辨識發生之後執行動作。</span><span class="sxs-lookup"><span data-stu-id="bfc36-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="bfc36-111">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="bfc36-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="bfc36-112">釋放在 ELS 文字辨識操作期間配置的記憶體和資源。</span><span class="sxs-lookup"><span data-stu-id="bfc36-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="bfc36-113">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="bfc36-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="bfc36-114">釋放配置給應用程式的記憶體和資源，以與一或多個 ELS 服務互動。</span><span class="sxs-lookup"><span data-stu-id="bfc36-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="bfc36-115">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="bfc36-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="bfc36-116">根據應用程式指定的準則，取得可用的 ELS 平臺支援服務清單，以及相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="bfc36-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="bfc36-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="bfc36-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="bfc36-118">在 ELS 服務上呼叫以辨識文字。</span><span class="sxs-lookup"><span data-stu-id="bfc36-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



