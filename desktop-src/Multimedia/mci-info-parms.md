---
title: 'MCI_INFO_PARMS 結構 (Mciapi .h) '
description: MCI \_ info \_ PARMS 結構包含 mci information 命令的資訊 \_ 。
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466925"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="3116e-104">MCI \_ 資訊 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="3116e-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="3116e-105">**Mci \_ info \_ PARMS** 結構包含 mci information 命令的 [**資訊 \_**](mci-info.md) 。</span><span class="sxs-lookup"><span data-stu-id="3116e-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3116e-106">語法</span><span class="sxs-lookup"><span data-stu-id="3116e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="3116e-107">成員</span><span class="sxs-lookup"><span data-stu-id="3116e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3116e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="3116e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3116e-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3116e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3116e-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="3116e-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="3116e-111">傳回字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3116e-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="3116e-112">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="3116e-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="3116e-113">傳回字串的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3116e-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3116e-114">備註</span><span class="sxs-lookup"><span data-stu-id="3116e-114">Remarks</span></span>

<span data-ttu-id="3116e-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="3116e-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3116e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3116e-116">Requirements</span></span>



| <span data-ttu-id="3116e-117">需求</span><span class="sxs-lookup"><span data-stu-id="3116e-117">Requirement</span></span> | <span data-ttu-id="3116e-118">值</span><span class="sxs-lookup"><span data-stu-id="3116e-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3116e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3116e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3116e-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3116e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3116e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3116e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3116e-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3116e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3116e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3116e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3116e-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3116e-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3116e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3116e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3116e-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="3116e-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3116e-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="3116e-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3116e-128">**MCI \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3116e-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="3116e-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3116e-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

