---
title: 'MCI_VCR_PLAY_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 播放 \_ PARMS 結構包含適用于 \_ video/卡帶燒錄機之 mci play 命令的參數。
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- MCI_VCR_PLAY_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934484"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="0661a-104">MCI \_ VCR \_ 播放 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="0661a-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="0661a-105">**Mci \_ VCR \_ 播放 \_ PARMS** 結構包含適用于 video/卡帶燒錄機之 [**mci \_ play**](mci-play.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="0661a-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="0661a-106">語法</span><span class="sxs-lookup"><span data-stu-id="0661a-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="0661a-107">成員</span><span class="sxs-lookup"><span data-stu-id="0661a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0661a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0661a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0661a-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0661a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0661a-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="0661a-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="0661a-111">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="0661a-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="0661a-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="0661a-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="0661a-113">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="0661a-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="0661a-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="0661a-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="0661a-115">影響 [**MCI \_ 播放**](mci-play.md) 或 [**MCI \_ 提示**](mci-cue.md) 命令的時間值。</span><span class="sxs-lookup"><span data-stu-id="0661a-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="0661a-116">在 [**MCI \_ 播放**](mci-play-parms.md)中，這是開始播放的時間。</span><span class="sxs-lookup"><span data-stu-id="0661a-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="0661a-117">對於 **MCI \_ 提示**，這是 Cued 裝置到達 **dwFrom** 中指定位置的時間。</span><span class="sxs-lookup"><span data-stu-id="0661a-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0661a-118">備註</span><span class="sxs-lookup"><span data-stu-id="0661a-118">Remarks</span></span>

<span data-ttu-id="0661a-119">以目前時間格式指定位置。</span><span class="sxs-lookup"><span data-stu-id="0661a-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="0661a-120">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="0661a-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0661a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0661a-121">Requirements</span></span>



| <span data-ttu-id="0661a-122">需求</span><span class="sxs-lookup"><span data-stu-id="0661a-122">Requirement</span></span> | <span data-ttu-id="0661a-123">值</span><span class="sxs-lookup"><span data-stu-id="0661a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0661a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0661a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0661a-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0661a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0661a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0661a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0661a-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0661a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0661a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0661a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0661a-129"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="0661a-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0661a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0661a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0661a-131">**Mci**</span><span class="sxs-lookup"><span data-stu-id="0661a-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0661a-132">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="0661a-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0661a-133">**MCI \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="0661a-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="0661a-134">**MCI \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="0661a-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="0661a-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0661a-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

