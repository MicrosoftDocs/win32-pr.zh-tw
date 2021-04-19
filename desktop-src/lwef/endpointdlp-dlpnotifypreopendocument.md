---
description: 在起始開啟的作業之前，為系統提供檔的相關資訊。
title: 'DlpNotifyPreOpenDocument 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495469"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="88292-103">DlpNotifyPreOpenDocument 函式</span><span class="sxs-lookup"><span data-stu-id="88292-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="88292-104">在起始開啟的作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88292-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="88292-105">語法</span><span class="sxs-lookup"><span data-stu-id="88292-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="88292-106">參數</span><span class="sxs-lookup"><span data-stu-id="88292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88292-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88292-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88292-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要開啟之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88292-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="88292-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="88292-109">Return value</span></span>

<span data-ttu-id="88292-110">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="88292-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="88292-111">備註</span><span class="sxs-lookup"><span data-stu-id="88292-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="88292-112">需求</span><span class="sxs-lookup"><span data-stu-id="88292-112">Requirements</span></span>



| <span data-ttu-id="88292-113">需求</span><span class="sxs-lookup"><span data-stu-id="88292-113">Requirement</span></span>          |    <span data-ttu-id="88292-114">值</span><span class="sxs-lookup"><span data-stu-id="88292-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88292-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88292-115">Minimum supported client</span></span><br/> | <span data-ttu-id="88292-116">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="88292-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="88292-117">DLL</span><span class="sxs-lookup"><span data-stu-id="88292-117">DLL</span></span><br/>                      | <span data-ttu-id="88292-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="88292-118">EndpointDlp.dll</span></span> |