---
description: 指定與端點 DLP 操作相關聯之檔的相關資訊。
title: 'DLP_DOCUMENT_INFO 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495542"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="7deb2-103">DLP_DOCUMENT_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="7deb2-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="7deb2-104">指定與端點 DLP 操作相關聯之檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7deb2-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7deb2-105">語法</span><span class="sxs-lookup"><span data-stu-id="7deb2-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="7deb2-106">成員</span><span class="sxs-lookup"><span data-stu-id="7deb2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7deb2-107">*版本* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7deb2-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deb2-108">指定 API 版本的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="7deb2-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="7deb2-109">此值應該一律為 **DLP_DOCUMENT_INFO_V_LATEST**。</span><span class="sxs-lookup"><span data-stu-id="7deb2-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="7deb2-110">此常數定義于「 [端點資料遺失防止](endpointdlp-endpoint-data-loss-prevention.md)」一文中的 endpointdlp 範例頭檔案清單中。</span><span class="sxs-lookup"><span data-stu-id="7deb2-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7deb2-111">*PersistentFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7deb2-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deb2-112">LPCWSTR，指定檔的原始路徑。</span><span class="sxs-lookup"><span data-stu-id="7deb2-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7deb2-113">*LocalFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7deb2-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7deb2-114">LPCWSTR，指定檔之實際備份檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7deb2-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="7deb2-115">備註</span><span class="sxs-lookup"><span data-stu-id="7deb2-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="7deb2-116">需求</span><span class="sxs-lookup"><span data-stu-id="7deb2-116">Requirements</span></span>



| <span data-ttu-id="7deb2-117">需求</span><span class="sxs-lookup"><span data-stu-id="7deb2-117">Requirement</span></span>          |    <span data-ttu-id="7deb2-118">值</span><span class="sxs-lookup"><span data-stu-id="7deb2-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7deb2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7deb2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7deb2-120">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="7deb2-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

