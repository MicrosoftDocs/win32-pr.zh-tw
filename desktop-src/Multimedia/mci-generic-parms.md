---
title: 'MCI_GENERIC_PARMS 結構 (Mciapi .h) '
description: MCI \_ 泛型 \_ PARMS 結構包含接收通知訊息的視窗控制碼。 此結構用於具有空白參數清單的 MCI 命令訊息。
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464984"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="2f452-105">MCI \_ 一般 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="2f452-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="2f452-106">**MCI \_ 泛型 \_ PARMS** 結構包含接收通知訊息的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f452-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="2f452-107">此結構用於具有空白參數清單的 MCI 命令訊息。</span><span class="sxs-lookup"><span data-stu-id="2f452-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f452-108">語法</span><span class="sxs-lookup"><span data-stu-id="2f452-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="2f452-109">成員</span><span class="sxs-lookup"><span data-stu-id="2f452-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f452-110">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="2f452-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2f452-111">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2f452-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f452-112">備註</span><span class="sxs-lookup"><span data-stu-id="2f452-112">Remarks</span></span>

<span data-ttu-id="2f452-113">**Mci \_ CLOSE \_ PARMS** 和 **Mci \_ 認識 \_ PARMS** 結構與 **mci \_ 一般 \_ PARMS** 結構相同。</span><span class="sxs-lookup"><span data-stu-id="2f452-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="2f452-114">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="2f452-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f452-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f452-115">Requirements</span></span>



| <span data-ttu-id="2f452-116">需求</span><span class="sxs-lookup"><span data-stu-id="2f452-116">Requirement</span></span> | <span data-ttu-id="2f452-117">值</span><span class="sxs-lookup"><span data-stu-id="2f452-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f452-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f452-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f452-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f452-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f452-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f452-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f452-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f452-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f452-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2f452-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f452-123"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f452-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f452-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f452-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f452-125">**Mci**</span><span class="sxs-lookup"><span data-stu-id="2f452-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f452-126">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="2f452-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="2f452-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f452-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

