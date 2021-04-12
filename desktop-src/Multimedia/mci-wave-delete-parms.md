---
title: 'MCI_WAVE_DELETE_PARMS 結構 (Mciapi .h) '
description: MCI \_ WAVE \_ delete \_ PARMS 結構包含 WAVE \_ -音訊裝置的 mci delete 命令的位置資訊。
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- MCI_WAVE_DELETE_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464620"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="ab7b9-104">MCI \_ WAVE \_ 刪除 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="ab7b9-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="ab7b9-105">**Mci \_ WAVE \_ delete \_ PARMS** 結構包含 WAVE-音訊裝置的 [**mci \_ delete**](mci-delete.md)命令的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="ab7b9-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7b9-106">語法</span><span class="sxs-lookup"><span data-stu-id="ab7b9-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="ab7b9-107">成員</span><span class="sxs-lookup"><span data-stu-id="ab7b9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab7b9-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ab7b9-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab7b9-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ab7b9-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="ab7b9-111">要從中刪除的位置。</span><span class="sxs-lookup"><span data-stu-id="ab7b9-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="ab7b9-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="ab7b9-113">要刪除的位置。</span><span class="sxs-lookup"><span data-stu-id="ab7b9-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab7b9-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab7b9-114">Remarks</span></span>

<span data-ttu-id="ab7b9-115">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="ab7b9-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7b9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab7b9-116">Requirements</span></span>



| <span data-ttu-id="ab7b9-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab7b9-117">Requirement</span></span> | <span data-ttu-id="ab7b9-118">值</span><span class="sxs-lookup"><span data-stu-id="ab7b9-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7b9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab7b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7b9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7b9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ab7b9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab7b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7b9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7b9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab7b9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab7b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7b9-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7b9-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7b9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab7b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7b9-126">**Mci**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ab7b9-127">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ab7b9-128">**MCI \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="ab7b9-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="ab7b9-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab7b9-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

