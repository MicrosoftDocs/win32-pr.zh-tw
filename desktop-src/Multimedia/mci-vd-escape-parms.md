---
title: 'MCI_VD_ESCAPE_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ ESCAPE \_ PARMS 結構包含傳送至裝置的命令，用於 VIDEODISC 裝置的 MCI \_ ESCAPE 命令。
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966105"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="2bfe4-104">MCI \_ VD \_ ESCAPE \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="2bfe4-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="2bfe4-105">**Mci \_ VD \_ ESCAPE \_ PARMS** 結構包含傳送至裝置的命令，用於 videodisc 裝置的 [**MCI \_ ESCAPE**](mci-escape.md)命令。</span><span class="sxs-lookup"><span data-stu-id="2bfe4-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bfe4-106">語法</span><span class="sxs-lookup"><span data-stu-id="2bfe4-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="2bfe4-107">成員</span><span class="sxs-lookup"><span data-stu-id="2bfe4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2bfe4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2bfe4-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2bfe4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2bfe4-110">**lpstrCommand**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="2bfe4-111">要傳送至裝置的命令。</span><span class="sxs-lookup"><span data-stu-id="2bfe4-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bfe4-112">備註</span><span class="sxs-lookup"><span data-stu-id="2bfe4-112">Remarks</span></span>

<span data-ttu-id="2bfe4-113">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="2bfe4-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bfe4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bfe4-114">Requirements</span></span>



| <span data-ttu-id="2bfe4-115">需求</span><span class="sxs-lookup"><span data-stu-id="2bfe4-115">Requirement</span></span> | <span data-ttu-id="2bfe4-116">值</span><span class="sxs-lookup"><span data-stu-id="2bfe4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfe4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bfe4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2bfe4-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bfe4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2bfe4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bfe4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2bfe4-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bfe4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2bfe4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2bfe4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bfe4-122"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bfe4-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bfe4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bfe4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bfe4-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2bfe4-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2bfe4-126">**MCI \_ ESCAPE**</span><span class="sxs-lookup"><span data-stu-id="2bfe4-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="2bfe4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bfe4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

