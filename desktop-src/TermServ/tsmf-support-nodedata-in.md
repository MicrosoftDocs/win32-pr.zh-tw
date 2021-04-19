---
title: TSMF_SUPPORT_NODEDATA_IN 結構
description: 在 TSMF 中使用 \_ ， \_ \_ 可支援結構中的資料，以包含支援之媒體格式的相關資訊。
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN 結構遠端桌面服務
- PTSMF_SUPPORT_NODEDATA_IN 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969984"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="8daa1-105">\_ \_ \_ 結構中的 TSMF 支援 NODEDATA</span><span class="sxs-lookup"><span data-stu-id="8daa1-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="8daa1-106">在 TSMF 中使用，可 [**\_ 支援結構 \_ \_ 中的資料**](tsmf-support-data-in.md) ，以包含支援之媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8daa1-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="8daa1-107">語法</span><span class="sxs-lookup"><span data-stu-id="8daa1-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="8daa1-108">成員</span><span class="sxs-lookup"><span data-stu-id="8daa1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8daa1-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="8daa1-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="8daa1-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8daa1-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8daa1-111">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="8daa1-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="8daa1-112">節點。</span><span class="sxs-lookup"><span data-stu-id="8daa1-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="8daa1-113">**numMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="8daa1-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="8daa1-114">媒體格式結構的數目。</span><span class="sxs-lookup"><span data-stu-id="8daa1-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="8daa1-115">**...**</span><span class="sxs-lookup"><span data-stu-id="8daa1-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="8daa1-116">定義音訊或影片媒體格式的結構數目不定。</span><span class="sxs-lookup"><span data-stu-id="8daa1-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="8daa1-117">**FormatType** 可為音訊 **格式化 \_ WaveFormatEx** 或影片的 **格式 \_ MFVideoFormat** 。</span><span class="sxs-lookup"><span data-stu-id="8daa1-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="8daa1-118">如需此結構的詳細資訊，請參閱 [TS \_ AM \_ 媒體 \_ 類型結構](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934)。</span><span class="sxs-lookup"><span data-stu-id="8daa1-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8daa1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8daa1-119">Requirements</span></span>



| <span data-ttu-id="8daa1-120">需求</span><span class="sxs-lookup"><span data-stu-id="8daa1-120">Requirement</span></span> | <span data-ttu-id="8daa1-121">值</span><span class="sxs-lookup"><span data-stu-id="8daa1-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="8daa1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8daa1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8daa1-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="8daa1-123">None supported</span></span><br/>         |
| <span data-ttu-id="8daa1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8daa1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8daa1-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8daa1-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8daa1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8daa1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8daa1-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="8daa1-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="8daa1-128">**TSMF \_ \_ \_ 中的支援資料**</span><span class="sxs-lookup"><span data-stu-id="8daa1-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

