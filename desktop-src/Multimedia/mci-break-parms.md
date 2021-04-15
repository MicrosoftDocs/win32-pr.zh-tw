---
title: 'MCI_BREAK_PARMS 結構 (Mciapi .h) '
description: MCI \_ break \_ PARMS 結構包含了 mci break 命令的虛擬金鑰程式碼和視窗資訊 \_ 。
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508476"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="dc8c4-104">MCI \_ BREAK \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="dc8c4-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="dc8c4-105">**Mci \_ break \_ PARMS** 結構包含了 [**mci \_ break**](mci-break.md)命令的虛擬金鑰程式碼和視窗資訊。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8c4-106">語法</span><span class="sxs-lookup"><span data-stu-id="dc8c4-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="dc8c4-107">成員</span><span class="sxs-lookup"><span data-stu-id="dc8c4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc8c4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="dc8c4-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="dc8c4-110">**nVirtKey**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="dc8c4-111">Break 鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="dc8c4-112">**hwndBreak**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="dc8c4-113">視窗的控制碼，必須是中斷偵測的目前視窗。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc8c4-114">備註</span><span class="sxs-lookup"><span data-stu-id="dc8c4-114">Remarks</span></span>

<span data-ttu-id="dc8c4-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="dc8c4-116">以下是定義的旗標：</span><span class="sxs-lookup"><span data-stu-id="dc8c4-116">The following flags are defined:</span></span>

<span data-ttu-id="dc8c4-117">MCI \_ BREAK \_ HWND</span><span class="sxs-lookup"><span data-stu-id="dc8c4-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="dc8c4-118">驗證 **hwndBreak** 成員，指定必須有焦點才能啟用中斷偵測的視窗。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="dc8c4-119">MCI \_ 中斷 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="dc8c4-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="dc8c4-120">驗證 **nVirtKey** 成員，其指定要用於 break 索引鍵的虛擬機器碼程式碼。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="dc8c4-121">MCI \_ 中斷 \_</span><span class="sxs-lookup"><span data-stu-id="dc8c4-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="dc8c4-122">停用任何現有的 break 鍵。</span><span class="sxs-lookup"><span data-stu-id="dc8c4-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc8c4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc8c4-123">Requirements</span></span>



| <span data-ttu-id="dc8c4-124">需求</span><span class="sxs-lookup"><span data-stu-id="dc8c4-124">Requirement</span></span> | <span data-ttu-id="dc8c4-125">值</span><span class="sxs-lookup"><span data-stu-id="dc8c4-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8c4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc8c4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc8c4-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc8c4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dc8c4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc8c4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc8c4-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc8c4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc8c4-130">標頭</span><span class="sxs-lookup"><span data-stu-id="dc8c4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc8c4-131"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc8c4-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc8c4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc8c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8c4-133">**Mci**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dc8c4-134">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="dc8c4-135">**MCI \_ 斷路**</span><span class="sxs-lookup"><span data-stu-id="dc8c4-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="dc8c4-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc8c4-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

