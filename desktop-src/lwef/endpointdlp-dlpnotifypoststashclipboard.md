---
description: 提供隱藏專案剪貼簿作業完成後的系統狀態資訊。
title: 'DlpNotifyPostStashClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495474"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="05b01-103">DlpNotifyPostStashClipboard 函式</span><span class="sxs-lookup"><span data-stu-id="05b01-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="05b01-104">提供隱藏專案剪貼簿作業完成後的系統狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="05b01-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b01-105">語法</span><span class="sxs-lookup"><span data-stu-id="05b01-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="05b01-106">參數</span><span class="sxs-lookup"><span data-stu-id="05b01-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="05b01-107">*OpStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05b01-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05b01-108">[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含隱藏專案剪貼簿作業的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="05b01-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="05b01-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="05b01-109">Return value</span></span>

<span data-ttu-id="05b01-110">傳回 void。</span><span class="sxs-lookup"><span data-stu-id="05b01-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b01-111">備註</span><span class="sxs-lookup"><span data-stu-id="05b01-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="05b01-112">需求</span><span class="sxs-lookup"><span data-stu-id="05b01-112">Requirements</span></span>



| <span data-ttu-id="05b01-113">需求</span><span class="sxs-lookup"><span data-stu-id="05b01-113">Requirement</span></span>          |    <span data-ttu-id="05b01-114">值</span><span class="sxs-lookup"><span data-stu-id="05b01-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05b01-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05b01-115">Minimum supported client</span></span><br/> | <span data-ttu-id="05b01-116">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="05b01-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="05b01-117">DLL</span><span class="sxs-lookup"><span data-stu-id="05b01-117">DLL</span></span><br/>                      | <span data-ttu-id="05b01-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="05b01-118">EndpointDlp.dll</span></span> |