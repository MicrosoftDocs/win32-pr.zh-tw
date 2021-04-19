---
description: 指定有關端點 DLP 操作的狀態資訊。
title: 'DLP_POSTOP_STATUS 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495441"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="289cb-103">DLP_POSTOP_STATUS 結構</span><span class="sxs-lookup"><span data-stu-id="289cb-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="289cb-104">指定有關端點 DLP 操作的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="289cb-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="289cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="289cb-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="289cb-106">成員</span><span class="sxs-lookup"><span data-stu-id="289cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="289cb-107">*版本* \[在\]</span><span class="sxs-lookup"><span data-stu-id="289cb-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289cb-108">指定 API 版本的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="289cb-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="289cb-109">此值應該一律為 **DLP_POSTOP_STATUS_V_LATEST**。</span><span class="sxs-lookup"><span data-stu-id="289cb-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="289cb-110">此常數定義于[端點資料遺失預防措施](endpointdlp-endpoint-data-loss-prevention.md)中的 endpointdlp 範例頭檔案清單中</span><span class="sxs-lookup"><span data-stu-id="289cb-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="289cb-111">*OperationSuccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="289cb-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289cb-112">布林值，指出開啟作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="289cb-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="289cb-113">備註</span><span class="sxs-lookup"><span data-stu-id="289cb-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="289cb-114">需求</span><span class="sxs-lookup"><span data-stu-id="289cb-114">Requirements</span></span>



| <span data-ttu-id="289cb-115">需求</span><span class="sxs-lookup"><span data-stu-id="289cb-115">Requirement</span></span>          |    <span data-ttu-id="289cb-116">值</span><span class="sxs-lookup"><span data-stu-id="289cb-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="289cb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="289cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="289cb-118">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="289cb-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
