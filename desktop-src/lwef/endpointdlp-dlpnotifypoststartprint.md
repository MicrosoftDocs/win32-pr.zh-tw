---
description: 在列印工作開始後，為系統提供檔的相關資訊。
title: 'DlpNotifyPostStartPrint 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495477"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="60f51-103">DlpNotifyPostStartPrint 函式</span><span class="sxs-lookup"><span data-stu-id="60f51-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="60f51-104">在列印工作開始後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60f51-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f51-105">語法</span><span class="sxs-lookup"><span data-stu-id="60f51-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="60f51-106">參數</span><span class="sxs-lookup"><span data-stu-id="60f51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f51-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f51-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f51-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含與列印工作相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60f51-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="60f51-109">*PrintInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f51-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f51-110">[DLP_PRINT_INFO](endpointdlp-dlp_print_info.md)結構的指標，其中包含列印工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60f51-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="60f51-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="60f51-111">Return value</span></span>

<span data-ttu-id="60f51-112">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="60f51-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f51-113">備註</span><span class="sxs-lookup"><span data-stu-id="60f51-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="60f51-114">需求</span><span class="sxs-lookup"><span data-stu-id="60f51-114">Requirements</span></span>



| <span data-ttu-id="60f51-115">需求</span><span class="sxs-lookup"><span data-stu-id="60f51-115">Requirement</span></span>          |    <span data-ttu-id="60f51-116">值</span><span class="sxs-lookup"><span data-stu-id="60f51-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60f51-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60f51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60f51-118">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="60f51-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="60f51-119">DLL</span><span class="sxs-lookup"><span data-stu-id="60f51-119">DLL</span></span><br/>                      | <span data-ttu-id="60f51-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="60f51-120">EndpointDlp.dll</span></span> |