---
title: TSMF_SUPPORT_DATA_IN 結構
description: 包含媒體格式的相關資訊。 |TSMF_SUPPORT_DATA_IN 結構
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN 結構遠端桌面服務
- PTSMF_SUPPORT_DATA_IN 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998981"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="1909c-106">TSMF \_ 支援 \_ \_ 結構中的資料</span><span class="sxs-lookup"><span data-stu-id="1909c-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="1909c-107">包含媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1909c-107">Contains information about media formats.</span></span> <span data-ttu-id="1909c-108">在 **WRDS \_ QUERY \_ MF \_ 格式 \_ 支援** 查詢期間， [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)方法會使用此結構。</span><span class="sxs-lookup"><span data-stu-id="1909c-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="1909c-109">語法</span><span class="sxs-lookup"><span data-stu-id="1909c-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="1909c-110">成員</span><span class="sxs-lookup"><span data-stu-id="1909c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1909c-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="1909c-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="1909c-112">會話。</span><span class="sxs-lookup"><span data-stu-id="1909c-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="1909c-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="1909c-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="1909c-114">變數長度資料中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="1909c-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="1909c-115">**...**</span><span class="sxs-lookup"><span data-stu-id="1909c-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="1909c-116">包含媒體格式資料之結構的數目不定。</span><span class="sxs-lookup"><span data-stu-id="1909c-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1909c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1909c-117">Requirements</span></span>



| <span data-ttu-id="1909c-118">需求</span><span class="sxs-lookup"><span data-stu-id="1909c-118">Requirement</span></span> | <span data-ttu-id="1909c-119">值</span><span class="sxs-lookup"><span data-stu-id="1909c-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="1909c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1909c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1909c-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="1909c-121">None supported</span></span><br/>         |
| <span data-ttu-id="1909c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1909c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1909c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1909c-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1909c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1909c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1909c-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="1909c-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="1909c-126">**TSMF \_ 支援 \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="1909c-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





