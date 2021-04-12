---
title: 'MCI_OVLY_RECT_PARMS 結構 (Mciapi .h) '
description: MCI \_ OVLY \_ RECT \_ PARMS 結構包含 MCI PUT 和 mci 的位置資訊，其中包含 \_ \_ 適用于影片重迭裝置的命令。
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464225"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="fd1f2-104">MCI \_ OVLY \_ RECT \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="fd1f2-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="fd1f2-105">**Mci \_ OVLY \_ RECT \_ PARMS** 結構包含 [**mci \_ PUT**](mci-put.md)和 mci 的位置資訊， [**\_ 其中**](mci-where.md)包含適用于影片重迭裝置的命令。</span><span class="sxs-lookup"><span data-stu-id="fd1f2-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1f2-106">語法</span><span class="sxs-lookup"><span data-stu-id="fd1f2-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="fd1f2-107">成員</span><span class="sxs-lookup"><span data-stu-id="fd1f2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd1f2-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="fd1f2-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fd1f2-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="fd1f2-110">**鋼筋混凝土**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="fd1f2-111">包含位置資訊的矩形。</span><span class="sxs-lookup"><span data-stu-id="fd1f2-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="fd1f2-112">在 MCI 中，[矩形](/previous-versions//ms536136(v=vs.85))結構的處理方式不同于 Windows 的其他部分;在 MCI 中， **.rc** 會包含矩形和 rc 的寬度 **。下方** 包含其高度。</span><span class="sxs-lookup"><span data-stu-id="fd1f2-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd1f2-113">備註</span><span class="sxs-lookup"><span data-stu-id="fd1f2-113">Remarks</span></span>

<span data-ttu-id="fd1f2-114">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="fd1f2-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1f2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd1f2-115">Requirements</span></span>



| <span data-ttu-id="fd1f2-116">需求</span><span class="sxs-lookup"><span data-stu-id="fd1f2-116">Requirement</span></span> | <span data-ttu-id="fd1f2-117">值</span><span class="sxs-lookup"><span data-stu-id="fd1f2-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1f2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd1f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1f2-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd1f2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fd1f2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd1f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1f2-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd1f2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd1f2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fd1f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1f2-123"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1f2-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1f2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd1f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1f2-125">**Mci**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fd1f2-126">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="fd1f2-127">**MCI \_ PUT**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="fd1f2-128">**MCI \_ ，其中**</span><span class="sxs-lookup"><span data-stu-id="fd1f2-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="fd1f2-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd1f2-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fd1f2-130">[矩形](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd1f2-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

