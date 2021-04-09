---
title: 'MCI_SEEK_PARMS 結構 (Mciapi .h) '
description: MCI \_ seek \_ PARMS 結構包含 mci 搜尋命令的位置資訊 \_ 。
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- MCI_SEEK_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685654"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="71511-104">MCI \_ 搜尋 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="71511-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="71511-105">**Mci \_ seek \_ PARMS** 結構包含 [**mci \_ 搜尋**](mci-seek.md)命令的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="71511-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="71511-106">語法</span><span class="sxs-lookup"><span data-stu-id="71511-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="71511-107">成員</span><span class="sxs-lookup"><span data-stu-id="71511-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="71511-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="71511-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="71511-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="71511-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="71511-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="71511-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="71511-111">要搜尋的位置。</span><span class="sxs-lookup"><span data-stu-id="71511-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71511-112">備註</span><span class="sxs-lookup"><span data-stu-id="71511-112">Remarks</span></span>

<span data-ttu-id="71511-113">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="71511-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="71511-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="71511-114">Requirements</span></span>



| <span data-ttu-id="71511-115">需求</span><span class="sxs-lookup"><span data-stu-id="71511-115">Requirement</span></span> | <span data-ttu-id="71511-116">值</span><span class="sxs-lookup"><span data-stu-id="71511-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71511-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71511-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71511-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71511-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="71511-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71511-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71511-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71511-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71511-121">標頭</span><span class="sxs-lookup"><span data-stu-id="71511-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="71511-122"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="71511-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71511-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71511-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71511-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="71511-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="71511-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="71511-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="71511-126">**MCI \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="71511-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="71511-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71511-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

