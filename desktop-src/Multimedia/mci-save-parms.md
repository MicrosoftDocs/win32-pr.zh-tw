---
title: 'MCI_SAVE_PARMS 結構 (Mciapi .h) '
description: MCI \_ save \_ PARMS 結構包含了 mci save 命令的檔案名資訊 \_ 。
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969758"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="069a1-104">MCI \_ 儲存 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="069a1-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="069a1-105">**Mci \_ save \_ PARMS** 結構包含了 [**mci \_ save**](mci-save.md)命令的檔案名資訊。</span><span class="sxs-lookup"><span data-stu-id="069a1-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="069a1-106">語法</span><span class="sxs-lookup"><span data-stu-id="069a1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="069a1-107">成員</span><span class="sxs-lookup"><span data-stu-id="069a1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="069a1-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="069a1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="069a1-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="069a1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="069a1-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="069a1-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="069a1-111">要儲存的檔案名。</span><span class="sxs-lookup"><span data-stu-id="069a1-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="069a1-112">備註</span><span class="sxs-lookup"><span data-stu-id="069a1-112">Remarks</span></span>

<span data-ttu-id="069a1-113">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="069a1-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="069a1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="069a1-114">Requirements</span></span>



| <span data-ttu-id="069a1-115">需求</span><span class="sxs-lookup"><span data-stu-id="069a1-115">Requirement</span></span> | <span data-ttu-id="069a1-116">值</span><span class="sxs-lookup"><span data-stu-id="069a1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="069a1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="069a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="069a1-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="069a1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="069a1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="069a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="069a1-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="069a1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="069a1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="069a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="069a1-122"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="069a1-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069a1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="069a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069a1-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="069a1-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="069a1-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="069a1-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="069a1-126">**MCI \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="069a1-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="069a1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="069a1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

