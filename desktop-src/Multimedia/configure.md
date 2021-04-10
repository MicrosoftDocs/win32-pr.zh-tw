---
title: 設定命令
description: '[設定] 命令會顯示用來設定裝置的對話方塊。 數位影片裝置辨識此命令。'
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- 設定命令 Windows 多媒體
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685492"
---
# <a name="configure-command"></a><span data-ttu-id="122bf-105">設定命令</span><span class="sxs-lookup"><span data-stu-id="122bf-105">configure command</span></span>

<span data-ttu-id="122bf-106">[設定] 命令會顯示用來設定裝置的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="122bf-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="122bf-107">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="122bf-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="122bf-108">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="122bf-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="122bf-109">參數</span><span class="sxs-lookup"><span data-stu-id="122bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="122bf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="122bf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="122bf-111">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="122bf-111">Identifier of an MCI device.</span></span> <span data-ttu-id="122bf-112">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="122bf-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="122bf-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="122bf-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="122bf-114">可以是「等候」、「通知」或「測試」。</span><span class="sxs-lookup"><span data-stu-id="122bf-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="122bf-115">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="122bf-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="122bf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="122bf-116">Return Value</span></span>

<span data-ttu-id="122bf-117">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="122bf-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="122bf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="122bf-118">Requirements</span></span>



| <span data-ttu-id="122bf-119">需求</span><span class="sxs-lookup"><span data-stu-id="122bf-119">Requirement</span></span> | <span data-ttu-id="122bf-120">值</span><span class="sxs-lookup"><span data-stu-id="122bf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="122bf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="122bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="122bf-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="122bf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="122bf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="122bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="122bf-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="122bf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="122bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="122bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122bf-126">Mci</span><span class="sxs-lookup"><span data-stu-id="122bf-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="122bf-127">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="122bf-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

