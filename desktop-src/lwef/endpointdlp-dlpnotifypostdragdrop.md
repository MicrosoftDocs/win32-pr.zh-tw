---
description: 在拖放作業完成後，為系統提供檔的相關資訊。
title: 'DlpNotifyPostDragDrop 函式 (endpointdlp) '
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
ms.openlocfilehash: 468255cee3c3fef44e44dd033b541e317db3d268
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495506"
---
# <a name="dlpnotifypostdragdrop-function"></a><span data-ttu-id="1c020-103">DlpNotifyPostDragDrop 函式</span><span class="sxs-lookup"><span data-stu-id="1c020-103">DlpNotifyPostDragDrop function</span></span>

<span data-ttu-id="1c020-104">在拖放作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c020-104">Provides the system with information about a document after a drag drop operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c020-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c020-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="1c020-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c020-107">*DocumentInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c020-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c020-108">[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含與拖放作業相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c020-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1c020-109">*OpStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c020-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c020-110">[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含拖放的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1c020-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="1c020-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c020-111">Return value</span></span>

<span data-ttu-id="1c020-112">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="1c020-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c020-113">備註</span><span class="sxs-lookup"><span data-stu-id="1c020-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1c020-114">需求</span><span class="sxs-lookup"><span data-stu-id="1c020-114">Requirements</span></span>



| <span data-ttu-id="1c020-115">需求</span><span class="sxs-lookup"><span data-stu-id="1c020-115">Requirement</span></span>          |    <span data-ttu-id="1c020-116">值</span><span class="sxs-lookup"><span data-stu-id="1c020-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c020-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c020-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c020-118">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="1c020-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1c020-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1c020-119">DLL</span></span><br/>                      | <span data-ttu-id="1c020-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1c020-120">EndpointDlp.dll</span></span> |