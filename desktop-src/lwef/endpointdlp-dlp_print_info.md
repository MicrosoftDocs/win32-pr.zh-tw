---
description: 指定與端點 DLP 列印操作相關聯之檔的相關資訊。
title: 'DLP_PRINT_INFO 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495541"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="752e4-103">DLP_PRINT_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="752e4-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="752e4-104">指定與端點 DLP 列印操作相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="752e4-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="752e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="752e4-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="752e4-106">成員</span><span class="sxs-lookup"><span data-stu-id="752e4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="752e4-107">*版本* \[在\]</span><span class="sxs-lookup"><span data-stu-id="752e4-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752e4-108">指定 API 版本的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="752e4-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="752e4-109">此值應該一律為 **DLP_PRINT_INFO_V_LATEST**。</span><span class="sxs-lookup"><span data-stu-id="752e4-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="752e4-110">此常數定義于「 [端點資料遺失防止](endpointdlp-endpoint-data-loss-prevention.md)」一文中的 endpointdlp 範例頭檔案清單中。</span><span class="sxs-lookup"><span data-stu-id="752e4-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="752e4-111">*PrinterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="752e4-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752e4-112">識別目的地印表機的 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="752e4-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="752e4-113">*JobName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="752e4-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752e4-114">指定列印工作名稱的 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="752e4-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="752e4-115">*OutputFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="752e4-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752e4-116">LPCWSTR，指定輸出檔案在列印至檔案時的路徑。</span><span class="sxs-lookup"><span data-stu-id="752e4-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="752e4-117">備註</span><span class="sxs-lookup"><span data-stu-id="752e4-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="752e4-118">需求</span><span class="sxs-lookup"><span data-stu-id="752e4-118">Requirements</span></span>



| <span data-ttu-id="752e4-119">需求</span><span class="sxs-lookup"><span data-stu-id="752e4-119">Requirement</span></span>          |    <span data-ttu-id="752e4-120">值</span><span class="sxs-lookup"><span data-stu-id="752e4-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="752e4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="752e4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="752e4-122">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="752e4-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

