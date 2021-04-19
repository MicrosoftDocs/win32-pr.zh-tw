---
title: escape 命令
description: Escape 命令會將裝置特定資訊傳送至裝置。 Videodisc 裝置會辨識此命令。
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- escape 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967711"
---
# <a name="escape-command"></a><span data-ttu-id="891d8-105">escape 命令</span><span class="sxs-lookup"><span data-stu-id="891d8-105">escape command</span></span>

<span data-ttu-id="891d8-106">Escape 命令會將裝置特定資訊傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="891d8-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="891d8-107">Videodisc 裝置會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="891d8-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="891d8-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="891d8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="891d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="891d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891d8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="891d8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="891d8-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="891d8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="891d8-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="891d8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="891d8-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span><span class="sxs-lookup"><span data-stu-id="891d8-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="891d8-114">要傳送至裝置的自訂資訊。</span><span class="sxs-lookup"><span data-stu-id="891d8-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="891d8-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="891d8-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="891d8-116">可以是「等候」、「通知」或兩者。</span><span class="sxs-lookup"><span data-stu-id="891d8-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="891d8-117">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="891d8-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891d8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="891d8-118">Return Value</span></span>

<span data-ttu-id="891d8-119">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="891d8-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="891d8-120">範例</span><span class="sxs-lookup"><span data-stu-id="891d8-120">Examples</span></span>

<span data-ttu-id="891d8-121">下列命令會將 escape 字串 "SA" 傳送至 videodisc 裝置。</span><span class="sxs-lookup"><span data-stu-id="891d8-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="891d8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="891d8-122">Requirements</span></span>



| <span data-ttu-id="891d8-123">需求</span><span class="sxs-lookup"><span data-stu-id="891d8-123">Requirement</span></span> | <span data-ttu-id="891d8-124">值</span><span class="sxs-lookup"><span data-stu-id="891d8-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="891d8-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="891d8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="891d8-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="891d8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="891d8-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="891d8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="891d8-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="891d8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="891d8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="891d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891d8-130">Mci</span><span class="sxs-lookup"><span data-stu-id="891d8-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="891d8-131">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="891d8-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

