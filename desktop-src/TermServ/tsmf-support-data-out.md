---
title: TSMF_SUPPORT_DATA_OUT 結構
description: 包含媒體格式的相關資訊。 |TSMF_SUPPORT_DATA_OUT 結構
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT 結構遠端桌面服務
- PTSMF_SUPPORT_DATA_OUT 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945818"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="b3dc7-106">TSMF \_ 支援 \_ 資料 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="b3dc7-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="b3dc7-107">包含媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3dc7-107">Contains information about media formats.</span></span> <span data-ttu-id="b3dc7-108">在 **WRDS \_ QUERY \_ MF \_ 格式 \_ 支援** 查詢期間， [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)方法會使用此結構。</span><span class="sxs-lookup"><span data-stu-id="b3dc7-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3dc7-109">語法</span><span class="sxs-lookup"><span data-stu-id="b3dc7-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="b3dc7-110">成員</span><span class="sxs-lookup"><span data-stu-id="b3dc7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3dc7-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="b3dc7-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="b3dc7-112">這必須符合結構中對應 [**TSMF \_ 支援 \_ 資料 \_**](tsmf-support-data-in.md)中的 **guidMfSession** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3dc7-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3dc7-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="b3dc7-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b3dc7-114">變數長度資料中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="b3dc7-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="b3dc7-115">**...**</span><span class="sxs-lookup"><span data-stu-id="b3dc7-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="b3dc7-116">包含媒體格式資料之結構的數目不定。</span><span class="sxs-lookup"><span data-stu-id="b3dc7-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3dc7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3dc7-117">Requirements</span></span>



| <span data-ttu-id="b3dc7-118">需求</span><span class="sxs-lookup"><span data-stu-id="b3dc7-118">Requirement</span></span> | <span data-ttu-id="b3dc7-119">值</span><span class="sxs-lookup"><span data-stu-id="b3dc7-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b3dc7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3dc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3dc7-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3dc7-121">None supported</span></span><br/>         |
| <span data-ttu-id="b3dc7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3dc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3dc7-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3dc7-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3dc7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3dc7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dc7-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b3dc7-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b3dc7-126">**TSMF \_ 支援 \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="b3dc7-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





