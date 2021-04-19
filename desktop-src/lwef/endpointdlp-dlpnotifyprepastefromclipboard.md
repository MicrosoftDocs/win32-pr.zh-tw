---
description: 為系統提供檔的相關資訊，再開始貼上剪貼簿作業。
title: 'DlpNotifyPrePasteFromClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495430"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="ecd9e-103">DlpNotifyPrePasteFromClipboard 函式</span><span class="sxs-lookup"><span data-stu-id="ecd9e-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="ecd9e-104">為系統提供檔的相關資訊，再開始貼上剪貼簿作業。</span><span class="sxs-lookup"><span data-stu-id="ecd9e-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ecd9e-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="ecd9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="ecd9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecd9e-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ecd9e-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecd9e-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要貼上內容之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ecd9e-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="ecd9e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecd9e-109">Return value</span></span>

<span data-ttu-id="ecd9e-110">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="ecd9e-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecd9e-111">備註</span><span class="sxs-lookup"><span data-stu-id="ecd9e-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="ecd9e-112">需求</span><span class="sxs-lookup"><span data-stu-id="ecd9e-112">Requirements</span></span>



| <span data-ttu-id="ecd9e-113">需求</span><span class="sxs-lookup"><span data-stu-id="ecd9e-113">Requirement</span></span>          |    <span data-ttu-id="ecd9e-114">值</span><span class="sxs-lookup"><span data-stu-id="ecd9e-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd9e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecd9e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd9e-116">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="ecd9e-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="ecd9e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ecd9e-117">DLL</span></span><br/>                      | <span data-ttu-id="ecd9e-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="ecd9e-118">EndpointDlp.dll</span></span> |