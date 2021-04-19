---
description: 在起始拖放作業之前，為系統提供檔的相關資訊。
title: 'DlpNotifyPreDragDrop 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495470"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="249b4-103">DlpNotifyPreDragDrop 函式</span><span class="sxs-lookup"><span data-stu-id="249b4-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="249b4-104">在起始拖放作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="249b4-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="249b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="249b4-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="249b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="249b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249b4-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="249b4-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="249b4-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含與拖放作業相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="249b4-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="249b4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="249b4-109">Return value</span></span>

<span data-ttu-id="249b4-110">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="249b4-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="249b4-111">備註</span><span class="sxs-lookup"><span data-stu-id="249b4-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="249b4-112">需求</span><span class="sxs-lookup"><span data-stu-id="249b4-112">Requirements</span></span>



| <span data-ttu-id="249b4-113">需求</span><span class="sxs-lookup"><span data-stu-id="249b4-113">Requirement</span></span>          |    <span data-ttu-id="249b4-114">值</span><span class="sxs-lookup"><span data-stu-id="249b4-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="249b4-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="249b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="249b4-116">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="249b4-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="249b4-117">DLL</span><span class="sxs-lookup"><span data-stu-id="249b4-117">DLL</span></span><br/>                      | <span data-ttu-id="249b4-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="249b4-118">EndpointDlp.dll</span></span> |