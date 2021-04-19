---
description: 在起始「另存新檔」作業之前，為系統提供檔的相關資訊。
title: 'DlpNotifyPreSaveAsDocument 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495437"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="b1013-103">DlpNotifyPreSaveAsDocument 函式</span><span class="sxs-lookup"><span data-stu-id="b1013-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="b1013-104">在起始「另存新檔」作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b1013-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1013-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1013-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="b1013-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1013-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1013-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1013-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1013-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要儲存之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b1013-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b1013-109">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1013-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1013-110">**LPCWSTR** ，其中包含要儲存之檔的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="b1013-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b1013-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1013-111">Return value</span></span>

<span data-ttu-id="b1013-112">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="b1013-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1013-113">備註</span><span class="sxs-lookup"><span data-stu-id="b1013-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b1013-114">需求</span><span class="sxs-lookup"><span data-stu-id="b1013-114">Requirements</span></span>



| <span data-ttu-id="b1013-115">需求</span><span class="sxs-lookup"><span data-stu-id="b1013-115">Requirement</span></span>          |    <span data-ttu-id="b1013-116">值</span><span class="sxs-lookup"><span data-stu-id="b1013-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1013-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1013-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1013-118">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="b1013-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b1013-119">DLL</span><span class="sxs-lookup"><span data-stu-id="b1013-119">DLL</span></span><br/>                      | <span data-ttu-id="b1013-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b1013-120">EndpointDlp.dll</span></span> |