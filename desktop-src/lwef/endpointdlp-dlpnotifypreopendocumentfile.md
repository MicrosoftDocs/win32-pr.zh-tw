---
description: 在啟動開啟作業之前，為系統提供檔檔案的相關資訊。
title: 'DlpNotifyPreOpenDocumentFile 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495466"
---
# <a name="dlpnotifypreopendocumentfile-function"></a><span data-ttu-id="d089a-103">DlpNotifyPreOpenDocumentFile 函式</span><span class="sxs-lookup"><span data-stu-id="d089a-103">DlpNotifyPreOpenDocumentFile function</span></span>

<span data-ttu-id="d089a-104">在啟動開啟作業之前，為系統提供檔檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d089a-104">Provides the system with information about a document file before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d089a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d089a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="d089a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d089a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d089a-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d089a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d089a-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要開啟之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d089a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="d089a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d089a-109">Return value</span></span>

<span data-ttu-id="d089a-110">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="d089a-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="d089a-111">備註</span><span class="sxs-lookup"><span data-stu-id="d089a-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="d089a-112">需求</span><span class="sxs-lookup"><span data-stu-id="d089a-112">Requirements</span></span>



| <span data-ttu-id="d089a-113">需求</span><span class="sxs-lookup"><span data-stu-id="d089a-113">Requirement</span></span>          |    <span data-ttu-id="d089a-114">值</span><span class="sxs-lookup"><span data-stu-id="d089a-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d089a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d089a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d089a-116">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="d089a-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="d089a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d089a-117">DLL</span></span><br/>                      | <span data-ttu-id="d089a-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="d089a-118">EndpointDlp.dll</span></span> |