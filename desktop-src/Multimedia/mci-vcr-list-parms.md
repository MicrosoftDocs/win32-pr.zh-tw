---
title: 'MCI_VCR_LIST_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 清單 \_ PARMS 結構包含適用于 \_ 視頻磁帶燒錄機的 mci 清單命令參數。
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- MCI_VCR_LIST_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317439"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="c75d8-104">MCI \_ VCR \_ 清單 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="c75d8-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="c75d8-105">**Mci \_ VCR \_ 清單 \_ PARMS** 結構包含適用于視頻磁帶燒錄機的 [**mci \_ 清單**](mci-list.md)命令參數。</span><span class="sxs-lookup"><span data-stu-id="c75d8-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75d8-106">語法</span><span class="sxs-lookup"><span data-stu-id="c75d8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="c75d8-107">成員</span><span class="sxs-lookup"><span data-stu-id="c75d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c75d8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c75d8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c75d8-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c75d8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c75d8-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="c75d8-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="c75d8-111">傳回之資訊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c75d8-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="c75d8-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="c75d8-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c75d8-113">VCR 影片或音訊輸入的數目。</span><span class="sxs-lookup"><span data-stu-id="c75d8-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c75d8-114">備註</span><span class="sxs-lookup"><span data-stu-id="c75d8-114">Remarks</span></span>

<span data-ttu-id="c75d8-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="c75d8-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75d8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c75d8-116">Requirements</span></span>



| <span data-ttu-id="c75d8-117">需求</span><span class="sxs-lookup"><span data-stu-id="c75d8-117">Requirement</span></span> | <span data-ttu-id="c75d8-118">值</span><span class="sxs-lookup"><span data-stu-id="c75d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c75d8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c75d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c75d8-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c75d8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c75d8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c75d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c75d8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c75d8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c75d8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c75d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75d8-124"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="c75d8-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75d8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c75d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75d8-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="c75d8-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c75d8-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="c75d8-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c75d8-128">**MCI \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="c75d8-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="c75d8-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c75d8-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

