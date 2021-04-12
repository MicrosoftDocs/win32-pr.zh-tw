---
title: 'MCI_VD_PLAY_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ PLAY \_ PARMS 結構包含 VIDEODISC 裝置的 mci PLAY 命令的位置和速度資訊 \_ 。
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025138"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="adc98-104">MCI \_ VD \_ PLAY \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="adc98-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="adc98-105">**Mci \_ VD \_ PLAY \_ PARMS** 結構包含 videodisc 裝置的 [**mci \_ PLAY**](mci-play.md)命令的位置和速度資訊。</span><span class="sxs-lookup"><span data-stu-id="adc98-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc98-106">語法</span><span class="sxs-lookup"><span data-stu-id="adc98-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="adc98-107">成員</span><span class="sxs-lookup"><span data-stu-id="adc98-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="adc98-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="adc98-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="adc98-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="adc98-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="adc98-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="adc98-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="adc98-111">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="adc98-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="adc98-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="adc98-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="adc98-113">要播放的位置。</span><span class="sxs-lookup"><span data-stu-id="adc98-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="adc98-114">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="adc98-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="adc98-115">每秒畫面格的播放速度。</span><span class="sxs-lookup"><span data-stu-id="adc98-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adc98-116">備註</span><span class="sxs-lookup"><span data-stu-id="adc98-116">Remarks</span></span>

<span data-ttu-id="adc98-117">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="adc98-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="adc98-118">如果您不是使用擴充的資料成員，您可以使用 [**mci \_ play \_ PARMS**](mci-play-parms.md) 結構，而不是 **mci \_ VD \_ PLAY \_ PARMS** 。</span><span class="sxs-lookup"><span data-stu-id="adc98-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc98-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="adc98-119">Requirements</span></span>



| <span data-ttu-id="adc98-120">需求</span><span class="sxs-lookup"><span data-stu-id="adc98-120">Requirement</span></span> | <span data-ttu-id="adc98-121">值</span><span class="sxs-lookup"><span data-stu-id="adc98-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="adc98-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adc98-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adc98-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adc98-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adc98-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adc98-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adc98-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adc98-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="adc98-126">標頭</span><span class="sxs-lookup"><span data-stu-id="adc98-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="adc98-127"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="adc98-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc98-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adc98-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc98-129">**Mci**</span><span class="sxs-lookup"><span data-stu-id="adc98-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="adc98-130">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="adc98-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="adc98-131">**MCI \_ 播放**</span><span class="sxs-lookup"><span data-stu-id="adc98-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="adc98-132">**MCI \_ PLAY \_ PARMS**</span><span class="sxs-lookup"><span data-stu-id="adc98-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="adc98-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="adc98-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

