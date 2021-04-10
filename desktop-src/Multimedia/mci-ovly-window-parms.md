---
title: 'MCI_OVLY_WINDOW_PARMS 結構 (Mciapi .h) '
description: MCI \_ OVLY \_ WINDOW \_ PARMS 結構包含適用于影片重迭裝置之 mci \_ 視窗命令的視窗顯示資訊。
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933898"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="08e06-104">MCI \_ OVLY \_ 視窗 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="08e06-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="08e06-105">**Mci \_ OVLY \_ WINDOW \_ PARMS** 結構包含適用于影片重迭裝置之 [**mci \_ 視窗**](mci-window.md)命令的視窗顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="08e06-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e06-106">語法</span><span class="sxs-lookup"><span data-stu-id="08e06-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="08e06-107">成員</span><span class="sxs-lookup"><span data-stu-id="08e06-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="08e06-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="08e06-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="08e06-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="08e06-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="08e06-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="08e06-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="08e06-111">顯示視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="08e06-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="08e06-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="08e06-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="08e06-113">視窗-顯示命令。</span><span class="sxs-lookup"><span data-stu-id="08e06-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="08e06-114">**lpstrText**</span><span class="sxs-lookup"><span data-stu-id="08e06-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="08e06-115">視窗標題。</span><span class="sxs-lookup"><span data-stu-id="08e06-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08e06-116">備註</span><span class="sxs-lookup"><span data-stu-id="08e06-116">Remarks</span></span>

<span data-ttu-id="08e06-117">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="08e06-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e06-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="08e06-118">Requirements</span></span>



| <span data-ttu-id="08e06-119">需求</span><span class="sxs-lookup"><span data-stu-id="08e06-119">Requirement</span></span> | <span data-ttu-id="08e06-120">值</span><span class="sxs-lookup"><span data-stu-id="08e06-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08e06-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08e06-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08e06-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08e06-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="08e06-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08e06-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08e06-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08e06-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="08e06-125">標頭</span><span class="sxs-lookup"><span data-stu-id="08e06-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08e06-126"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="08e06-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e06-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08e06-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e06-128">**Mci**</span><span class="sxs-lookup"><span data-stu-id="08e06-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="08e06-129">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="08e06-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="08e06-130">**MCI \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="08e06-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="08e06-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08e06-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

