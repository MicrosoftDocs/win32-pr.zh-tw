---
title: 'MCI_CLOSE 命令 (Mmsystem .h) '
description: MCI \_ CLOSE 命令會釋放對裝置或檔案的存取權。 所有裝置都會辨識此命令。
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094392"
---
# <a name="mci_close-command"></a><span data-ttu-id="66d9f-105">MCI \_ 關閉命令</span><span class="sxs-lookup"><span data-stu-id="66d9f-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="66d9f-106">MCI \_ CLOSE 命令會釋放對裝置或檔案的存取權。</span><span class="sxs-lookup"><span data-stu-id="66d9f-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="66d9f-107">所有裝置都會辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="66d9f-107">All devices recognize this command.</span></span>

<span data-ttu-id="66d9f-108">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="66d9f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="66d9f-109">參數</span><span class="sxs-lookup"><span data-stu-id="66d9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d9f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="66d9f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="66d9f-111">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="66d9f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="66d9f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="66d9f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="66d9f-113">MCI \_ 通知或 mci \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="66d9f-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="66d9f-114">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="66d9f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="66d9f-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span><span class="sxs-lookup"><span data-stu-id="66d9f-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="66d9f-116">[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="66d9f-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="66d9f-117"> (您也可以使用 **MCI \_ CLOSE \_ PARMS** 結構。</span><span class="sxs-lookup"><span data-stu-id="66d9f-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="66d9f-118">如需詳細資訊，請參閱 **MCI \_ 一般 \_ PARMS** 的批註。 ) </span><span class="sxs-lookup"><span data-stu-id="66d9f-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d9f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="66d9f-119">Return Value</span></span>

<span data-ttu-id="66d9f-120">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="66d9f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d9f-121">備註</span><span class="sxs-lookup"><span data-stu-id="66d9f-121">Remarks</span></span>

<span data-ttu-id="66d9f-122">結束應用程式而不關閉已開啟的任何 MCI 裝置，可能會讓裝置無法存取。</span><span class="sxs-lookup"><span data-stu-id="66d9f-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="66d9f-123">當您的應用程式完成時，您的應用程式應該明確地關閉每個裝置或檔案。</span><span class="sxs-lookup"><span data-stu-id="66d9f-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="66d9f-124">當裝置或所有相關檔案的所有實例都已關閉時，MCI 會卸載裝置。</span><span class="sxs-lookup"><span data-stu-id="66d9f-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d9f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="66d9f-125">Requirements</span></span>



| <span data-ttu-id="66d9f-126">需求</span><span class="sxs-lookup"><span data-stu-id="66d9f-126">Requirement</span></span> | <span data-ttu-id="66d9f-127">值</span><span class="sxs-lookup"><span data-stu-id="66d9f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d9f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66d9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66d9f-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66d9f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66d9f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66d9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66d9f-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66d9f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="66d9f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="66d9f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d9f-133"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="66d9f-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d9f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66d9f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d9f-135">Mci</span><span class="sxs-lookup"><span data-stu-id="66d9f-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="66d9f-136">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="66d9f-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

