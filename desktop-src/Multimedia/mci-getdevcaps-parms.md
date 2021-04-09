---
title: 'MCI_GETDEVCAPS_PARMS 結構 (Mciapi .h) '
description: MCI \_ GETDEVCAPS \_ PARMS 結構包含 mci GETDEVCAPS 命令的裝置功能資訊 \_ 。
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- MCI_GETDEVCAPS_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024789"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="cce98-104">MCI \_ GETDEVCAPS \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="cce98-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="cce98-105">**Mci \_ GETDEVCAPS \_ PARMS** 結構包含 [**mci \_ GETDEVCAPS**](mci-getdevcaps.md)命令的裝置功能資訊。</span><span class="sxs-lookup"><span data-stu-id="cce98-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce98-106">語法</span><span class="sxs-lookup"><span data-stu-id="cce98-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="cce98-107">成員</span><span class="sxs-lookup"><span data-stu-id="cce98-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cce98-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="cce98-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cce98-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cce98-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cce98-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="cce98-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="cce98-111">包含結束時的資訊。</span><span class="sxs-lookup"><span data-stu-id="cce98-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="cce98-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="cce98-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="cce98-113">正在查詢的功能。</span><span class="sxs-lookup"><span data-stu-id="cce98-113">Capability being queried.</span></span> <span data-ttu-id="cce98-114">這個成員可以是 [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) 命令的參考資料中所列的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="cce98-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cce98-115">備註</span><span class="sxs-lookup"><span data-stu-id="cce98-115">Remarks</span></span>

<span data-ttu-id="cce98-116">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="cce98-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce98-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cce98-117">Requirements</span></span>



| <span data-ttu-id="cce98-118">需求</span><span class="sxs-lookup"><span data-stu-id="cce98-118">Requirement</span></span> | <span data-ttu-id="cce98-119">值</span><span class="sxs-lookup"><span data-stu-id="cce98-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cce98-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cce98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cce98-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cce98-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cce98-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cce98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cce98-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cce98-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cce98-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cce98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce98-125"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cce98-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce98-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cce98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce98-127">**Mci**</span><span class="sxs-lookup"><span data-stu-id="cce98-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cce98-128">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="cce98-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cce98-129">**MCI \_ GETDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="cce98-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="cce98-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cce98-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

