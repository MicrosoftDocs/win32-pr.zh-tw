---
title: 'MCI_SYSINFO_PARMS 結構 (Mciapi .h) '
description: MCI \_ SYSINFO \_ PARMS 結構包含 mci SYSINFO 命令的資訊 \_ 。
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969556"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="488f4-104">MCI \_ SYSINFO \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="488f4-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="488f4-105">**Mci \_ SYSINFO \_ PARMS** 結構包含 [**mci \_ SYSINFO**](mci-sysinfo.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="488f4-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="488f4-106">語法</span><span class="sxs-lookup"><span data-stu-id="488f4-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="488f4-107">成員</span><span class="sxs-lookup"><span data-stu-id="488f4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="488f4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="488f4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="488f4-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="488f4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="488f4-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="488f4-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="488f4-111">傳回字串之使用者提供的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="488f4-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="488f4-112"> \_ 使用 MCI SYSINFO QUANTITY 旗標時，也會使用它來傳回 DWORD 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="488f4-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="488f4-113">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="488f4-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="488f4-114">傳回緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="488f4-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="488f4-115">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="488f4-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="488f4-116">如果設定了 MCI \_ SYSINFO 開啟旗標，則會指出 mci 裝置表格或開啟的裝置清單中的裝置位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="488f4-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="488f4-117">**wDeviceType**</span><span class="sxs-lookup"><span data-stu-id="488f4-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="488f4-118">裝置類型。</span><span class="sxs-lookup"><span data-stu-id="488f4-118">Type of device.</span></span> <span data-ttu-id="488f4-119">此成員可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="488f4-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="488f4-120">備註</span><span class="sxs-lookup"><span data-stu-id="488f4-120">Remarks</span></span>

<span data-ttu-id="488f4-121">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="488f4-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="488f4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="488f4-122">Requirements</span></span>



| <span data-ttu-id="488f4-123">需求</span><span class="sxs-lookup"><span data-stu-id="488f4-123">Requirement</span></span> | <span data-ttu-id="488f4-124">值</span><span class="sxs-lookup"><span data-stu-id="488f4-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="488f4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="488f4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="488f4-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="488f4-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="488f4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="488f4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="488f4-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="488f4-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="488f4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="488f4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="488f4-130"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="488f4-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488f4-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="488f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488f4-132">**Mci**</span><span class="sxs-lookup"><span data-stu-id="488f4-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="488f4-133">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="488f4-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="488f4-134">**MCI \_ SYSINFO**</span><span class="sxs-lookup"><span data-stu-id="488f4-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="488f4-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="488f4-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

