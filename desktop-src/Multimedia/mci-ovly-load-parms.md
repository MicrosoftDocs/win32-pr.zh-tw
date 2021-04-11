---
title: 'MCI_OVLY_LOAD_PARMS 結構 (Mmsystem .h) '
description: MCI \_ OVLY \_ LOAD PARMS 結構包含適用于影片重迭裝置之 \_ MCI \_ LOAD 命令的資訊。
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024566"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="bf7a8-104">MCI \_ OVLY \_ LOAD \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="bf7a8-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="bf7a8-105">**Mci \_ OVLY \_ LOAD \_ PARMS** 結構包含適用于影片重迭裝置之 [**MCI \_ LOAD**](mci-load.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7a8-106">語法</span><span class="sxs-lookup"><span data-stu-id="bf7a8-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="bf7a8-107">成員</span><span class="sxs-lookup"><span data-stu-id="bf7a8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf7a8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bf7a8-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bf7a8-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="bf7a8-111">要載入之檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="bf7a8-112">**鋼筋混凝土**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="bf7a8-113">識別要更新的影片緩衝區區域。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="bf7a8-114">在 MCI 中，[矩形](/previous-versions//ms536136(v=vs.85))結構的處理方式不同于 Windows 的其他部分;在 MCI 中， **.rc** 會包含矩形和 rc 的寬度 **。下方** 包含其高度。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf7a8-115">備註</span><span class="sxs-lookup"><span data-stu-id="bf7a8-115">Remarks</span></span>

<span data-ttu-id="bf7a8-116">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="bf7a8-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7a8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf7a8-117">Requirements</span></span>



| <span data-ttu-id="bf7a8-118">需求</span><span class="sxs-lookup"><span data-stu-id="bf7a8-118">Requirement</span></span> | <span data-ttu-id="bf7a8-119">值</span><span class="sxs-lookup"><span data-stu-id="bf7a8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7a8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf7a8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7a8-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf7a8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bf7a8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf7a8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7a8-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf7a8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf7a8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bf7a8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7a8-125"><dt>Mmsystem。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a8-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7a8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf7a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7a8-127">**Mci**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bf7a8-128">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bf7a8-129">**MCI \_ 負載**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="bf7a8-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf7a8-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="bf7a8-131">[矩形](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf7a8-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

