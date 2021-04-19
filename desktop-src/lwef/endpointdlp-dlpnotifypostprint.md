---
description: 在列印工作完成後，為系統提供檔的相關資訊。
title: 'DlpNotifyPostPrint 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495481"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="e5cb6-103">DlpNotifyPostPrint 函式</span><span class="sxs-lookup"><span data-stu-id="e5cb6-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="e5cb6-104">在列印工作完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5cb6-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5cb6-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5cb6-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="e5cb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5cb6-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5cb6-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cb6-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含與列印工作相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5cb6-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="e5cb6-109">*PrintInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5cb6-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cb6-110">[DLP_PRINT_INFO](endpointdlp-dlp_print_info.md)結構的指標，其中包含列印工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5cb6-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="e5cb6-111">*OpStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5cb6-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cb6-112">[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含列印工作的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e5cb6-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="e5cb6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5cb6-113">Return value</span></span>

<span data-ttu-id="e5cb6-114">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="e5cb6-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5cb6-115">備註</span><span class="sxs-lookup"><span data-stu-id="e5cb6-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="e5cb6-116">需求</span><span class="sxs-lookup"><span data-stu-id="e5cb6-116">Requirements</span></span>



| <span data-ttu-id="e5cb6-117">需求</span><span class="sxs-lookup"><span data-stu-id="e5cb6-117">Requirement</span></span>          |    <span data-ttu-id="e5cb6-118">值</span><span class="sxs-lookup"><span data-stu-id="e5cb6-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cb6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5cb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5cb6-120">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="e5cb6-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="e5cb6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e5cb6-121">DLL</span></span><br/>                      | <span data-ttu-id="e5cb6-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="e5cb6-122">EndpointDlp.dll</span></span> |