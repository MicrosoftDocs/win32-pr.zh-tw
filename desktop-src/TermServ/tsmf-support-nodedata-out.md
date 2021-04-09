---
title: TSMF_SUPPORT_NODEDATA_OUT 結構
description: 在 TSMF 內使用 \_ \_ 可支援資料 \_ 輸出結構，以包含支援之媒體格式的相關資訊。
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT 結構遠端桌面服務
- PTSMF_SUPPORT_NODEDATA_OUT 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843840"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="0ea4d-105">TSMF \_ 支援 \_ NODEDATA \_ OUT 結構</span><span class="sxs-lookup"><span data-stu-id="0ea4d-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="0ea4d-106">在 TSMF 內使用可 [**\_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md) 結構，以包含支援之媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0ea4d-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="0ea4d-108">成員</span><span class="sxs-lookup"><span data-stu-id="0ea4d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ea4d-109">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-110">節點。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="0ea4d-111">**hrSupportStatus**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-112">是否支援 *clsidNewSink* 參數所識別的接收。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="0ea4d-113">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="0ea4d-114">0</span><span class="sxs-lookup"><span data-stu-id="0ea4d-114">0</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-115">不支援</span><span class="sxs-lookup"><span data-stu-id="0ea4d-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="0ea4d-116">1</span><span class="sxs-lookup"><span data-stu-id="0ea4d-116">1</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-117">支援</span><span class="sxs-lookup"><span data-stu-id="0ea4d-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="0ea4d-118">其他值則為未定義。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="0ea4d-119">**clsidNewSink**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-120">與媒體類型相關聯的接收。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="0ea4d-121">**supportedMediaTypeIndex**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="0ea4d-122">接收所支援之媒體類型的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="0ea4d-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ea4d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ea4d-123">Requirements</span></span>



| <span data-ttu-id="0ea4d-124">需求</span><span class="sxs-lookup"><span data-stu-id="0ea4d-124">Requirement</span></span> | <span data-ttu-id="0ea4d-125">值</span><span class="sxs-lookup"><span data-stu-id="0ea4d-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="0ea4d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ea4d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea4d-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="0ea4d-127">None supported</span></span><br/>         |
| <span data-ttu-id="0ea4d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ea4d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea4d-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ea4d-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ea4d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ea4d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea4d-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="0ea4d-132">**TSMF \_ 支援 \_ 資料 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0ea4d-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





