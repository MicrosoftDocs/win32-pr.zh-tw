---
description: 在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。
title: 'DlpNotifyPostSaveAsDocument 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495478"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="ed220-103">DlpNotifyPostSaveAsDocument 函式</span><span class="sxs-lookup"><span data-stu-id="ed220-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="ed220-104">在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed220-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed220-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed220-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="ed220-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed220-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed220-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed220-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed220-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含所儲存檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed220-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ed220-109">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed220-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed220-110">**LPCWSTR** ，其中包含所儲存檔的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="ed220-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ed220-111">*OpStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed220-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed220-112">[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含有關「另存新檔」作業的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ed220-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="ed220-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed220-113">Return value</span></span>

<span data-ttu-id="ed220-114">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="ed220-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed220-115">備註</span><span class="sxs-lookup"><span data-stu-id="ed220-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="ed220-116">需求</span><span class="sxs-lookup"><span data-stu-id="ed220-116">Requirements</span></span>



| <span data-ttu-id="ed220-117">需求</span><span class="sxs-lookup"><span data-stu-id="ed220-117">Requirement</span></span>          |    <span data-ttu-id="ed220-118">值</span><span class="sxs-lookup"><span data-stu-id="ed220-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed220-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed220-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed220-120">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="ed220-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="ed220-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ed220-121">DLL</span></span><br/>                      | <span data-ttu-id="ed220-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="ed220-122">EndpointDlp.dll</span></span> |