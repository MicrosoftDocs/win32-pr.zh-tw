---
title: 復原命令
description: '[復原] 命令會反轉最新成功的複製、剪下、刪除、復原或貼上命令所採取的動作。 數位影片裝置辨識此命令。'
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- 復原命令 Windows 多媒體
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025461"
---
# <a name="undo-command"></a><span data-ttu-id="6cd15-105">復原命令</span><span class="sxs-lookup"><span data-stu-id="6cd15-105">undo command</span></span>

<span data-ttu-id="6cd15-106">[復原] 命令會反轉最新成功的 [複製](copy.md)、 [剪](cut.md)下、 [刪除](delete.md)、復原或 [貼](paste.md) 上命令所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="6cd15-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="6cd15-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="6cd15-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6cd15-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6cd15-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6cd15-109">參數</span><span class="sxs-lookup"><span data-stu-id="6cd15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd15-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6cd15-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6cd15-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cd15-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6cd15-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="6cd15-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6cd15-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6cd15-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6cd15-114">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="6cd15-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6cd15-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd15-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd15-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cd15-116">Return Value</span></span>

<span data-ttu-id="6cd15-117">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6cd15-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd15-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cd15-118">Requirements</span></span>



| <span data-ttu-id="6cd15-119">需求</span><span class="sxs-lookup"><span data-stu-id="6cd15-119">Requirement</span></span> | <span data-ttu-id="6cd15-120">值</span><span class="sxs-lookup"><span data-stu-id="6cd15-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6cd15-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cd15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd15-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cd15-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6cd15-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cd15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd15-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cd15-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6cd15-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cd15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd15-126">Mci</span><span class="sxs-lookup"><span data-stu-id="6cd15-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6cd15-127">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="6cd15-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6cd15-128">copy</span><span class="sxs-lookup"><span data-stu-id="6cd15-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="6cd15-129">削減</span><span class="sxs-lookup"><span data-stu-id="6cd15-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="6cd15-130">delete</span><span class="sxs-lookup"><span data-stu-id="6cd15-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="6cd15-131">粘貼</span><span class="sxs-lookup"><span data-stu-id="6cd15-131">paste</span></span>](paste.md)
</dt> </dl>

 

