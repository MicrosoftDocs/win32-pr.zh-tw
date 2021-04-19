---
title: 'MCI_VCR_RECORD_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 記錄 \_ PARMS 結構包含適用于 \_ 視頻磁帶燒錄機之 mci 記錄命令的參數。
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968149"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="58dce-104">MCI \_ VCR \_ 記錄 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="58dce-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="58dce-105">**Mci \_ VCR \_ 記錄 \_ PARMS** 結構包含適用于視頻磁帶燒錄機之 [**mci \_ 記錄**](mci-record.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="58dce-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="58dce-106">語法</span><span class="sxs-lookup"><span data-stu-id="58dce-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="58dce-107">成員</span><span class="sxs-lookup"><span data-stu-id="58dce-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="58dce-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="58dce-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="58dce-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="58dce-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="58dce-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="58dce-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="58dce-111">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="58dce-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="58dce-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="58dce-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="58dce-113">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="58dce-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="58dce-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="58dce-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="58dce-115">影響 [**MCI \_ 記錄**](mci-record.md) 或 [**MCI \_ 提示**](mci-cue.md) 命令的時間值。</span><span class="sxs-lookup"><span data-stu-id="58dce-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="58dce-116">對於 **MCI \_ 記錄**，這是開始錄製的時間。</span><span class="sxs-lookup"><span data-stu-id="58dce-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="58dce-117">對於 **MCI \_ 提示**，這是 Cued 裝置到達 **dwFrom** 中指定位置的時間。</span><span class="sxs-lookup"><span data-stu-id="58dce-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58dce-118">備註</span><span class="sxs-lookup"><span data-stu-id="58dce-118">Remarks</span></span>

<span data-ttu-id="58dce-119">以目前時間格式指定位置。</span><span class="sxs-lookup"><span data-stu-id="58dce-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="58dce-120">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="58dce-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="58dce-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="58dce-121">Requirements</span></span>



| <span data-ttu-id="58dce-122">需求</span><span class="sxs-lookup"><span data-stu-id="58dce-122">Requirement</span></span> | <span data-ttu-id="58dce-123">值</span><span class="sxs-lookup"><span data-stu-id="58dce-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="58dce-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58dce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="58dce-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58dce-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="58dce-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58dce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="58dce-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58dce-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58dce-128">標頭</span><span class="sxs-lookup"><span data-stu-id="58dce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="58dce-129"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="58dce-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58dce-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58dce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58dce-131">**Mci**</span><span class="sxs-lookup"><span data-stu-id="58dce-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="58dce-132">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="58dce-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="58dce-133">**MCI \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="58dce-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="58dce-134">**MCI \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="58dce-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="58dce-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58dce-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

