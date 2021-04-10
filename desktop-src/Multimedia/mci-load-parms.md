---
title: 'MCI_LOAD_PARMS 結構 (Mmsystem .h) '
description: MCI \_ load \_ PARMS 結構包含要針對 MCI load 命令載入的檔案名 \_ 。
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686269"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="ead4f-104">MCI \_ LOAD \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="ead4f-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="ead4f-105">**Mci \_ load \_ PARMS** 結構包含要針對 [**MCI \_ load**](mci-load.md)命令載入的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ead4f-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead4f-106">語法</span><span class="sxs-lookup"><span data-stu-id="ead4f-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="ead4f-107">成員</span><span class="sxs-lookup"><span data-stu-id="ead4f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ead4f-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ead4f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ead4f-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ead4f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ead4f-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="ead4f-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="ead4f-111">要載入之檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ead4f-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ead4f-112">備註</span><span class="sxs-lookup"><span data-stu-id="ead4f-112">Remarks</span></span>

<span data-ttu-id="ead4f-113">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="ead4f-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead4f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ead4f-114">Requirements</span></span>



| <span data-ttu-id="ead4f-115">需求</span><span class="sxs-lookup"><span data-stu-id="ead4f-115">Requirement</span></span> | <span data-ttu-id="ead4f-116">值</span><span class="sxs-lookup"><span data-stu-id="ead4f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ead4f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ead4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ead4f-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ead4f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ead4f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ead4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ead4f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ead4f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ead4f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ead4f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead4f-122"><dt>Mmsystem。h</dt></span><span class="sxs-lookup"><span data-stu-id="ead4f-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead4f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ead4f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead4f-124">**Mci**</span><span class="sxs-lookup"><span data-stu-id="ead4f-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ead4f-125">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="ead4f-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ead4f-126">**MCI \_ 負載**</span><span class="sxs-lookup"><span data-stu-id="ead4f-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="ead4f-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ead4f-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

