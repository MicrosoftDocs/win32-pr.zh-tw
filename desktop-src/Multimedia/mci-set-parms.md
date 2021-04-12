---
title: 'MCI_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ set \_ PARMS 結構包含 mci set 命令的資訊 \_ 。
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- MCI_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024784"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="6026c-104">MCI \_ 設定 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="6026c-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="6026c-105">**Mci \_ set \_ PARMS** 結構包含 [**mci \_ set**](mci-set.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="6026c-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6026c-106">語法</span><span class="sxs-lookup"><span data-stu-id="6026c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="6026c-107">成員</span><span class="sxs-lookup"><span data-stu-id="6026c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6026c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6026c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6026c-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6026c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6026c-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="6026c-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="6026c-111">裝置的時間格式。</span><span class="sxs-lookup"><span data-stu-id="6026c-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="6026c-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="6026c-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="6026c-113">音訊輸出通道。</span><span class="sxs-lookup"><span data-stu-id="6026c-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6026c-114">備註</span><span class="sxs-lookup"><span data-stu-id="6026c-114">Remarks</span></span>

<span data-ttu-id="6026c-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="6026c-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6026c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6026c-116">Requirements</span></span>



| <span data-ttu-id="6026c-117">需求</span><span class="sxs-lookup"><span data-stu-id="6026c-117">Requirement</span></span> | <span data-ttu-id="6026c-118">值</span><span class="sxs-lookup"><span data-stu-id="6026c-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6026c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6026c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6026c-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6026c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6026c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6026c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6026c-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6026c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6026c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6026c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6026c-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6026c-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6026c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6026c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6026c-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="6026c-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6026c-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="6026c-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6026c-128">**MCI \_ 組**</span><span class="sxs-lookup"><span data-stu-id="6026c-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="6026c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6026c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

