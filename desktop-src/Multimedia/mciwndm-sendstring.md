---
title: 'MCIWNDM_SENDSTRING 訊息 (Vfw .h) '
description: MCIWNDM \_ SENDSTRING 訊息會以字串形式將 MCI 命令傳送給與 MCIWnd 視窗相關聯的裝置。 您可以使用 MCIWndSendString 宏明確地傳送此訊息。
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686154"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="0922c-105">MCIWNDM \_ SENDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="0922c-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="0922c-106">**MCIWNDM \_ SENDSTRING** 訊息會以字串形式將 MCI 命令傳送給與 MCIWnd 視窗相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="0922c-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="0922c-107">您可以使用 [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0922c-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="0922c-108">參數</span><span class="sxs-lookup"><span data-stu-id="0922c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0922c-109"><span id="sz"></span><span id="SZ"></span>*深圳*</span><span class="sxs-lookup"><span data-stu-id="0922c-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="0922c-110">要傳送至 MCI 裝置的字串命令。</span><span class="sxs-lookup"><span data-stu-id="0922c-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0922c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0922c-111">Return Value</span></span>

<span data-ttu-id="0922c-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0922c-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0922c-113">備註</span><span class="sxs-lookup"><span data-stu-id="0922c-113">Remarks</span></span>

<span data-ttu-id="0922c-114">**MCIWNDM \_ SENDSTRING** 的訊息處理常式會將裝置別名附加至您傳送至裝置的 MCI 命令。</span><span class="sxs-lookup"><span data-stu-id="0922c-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="0922c-115">因此，您不應該在使用 **MCIWNDM \_ SENDSTRING** 發出的 MCI 命令中使用任何別名。</span><span class="sxs-lookup"><span data-stu-id="0922c-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="0922c-116">若要取得包含命令結果的傳回字串，請傳送 [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0922c-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0922c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0922c-117">Requirements</span></span>



| <span data-ttu-id="0922c-118">需求</span><span class="sxs-lookup"><span data-stu-id="0922c-118">Requirement</span></span> | <span data-ttu-id="0922c-119">值</span><span class="sxs-lookup"><span data-stu-id="0922c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0922c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0922c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0922c-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0922c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0922c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0922c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0922c-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0922c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0922c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0922c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0922c-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="0922c-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0922c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0922c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0922c-127">**MCIWndSendString**</span><span class="sxs-lookup"><span data-stu-id="0922c-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="0922c-128">多媒體命令字串</span><span class="sxs-lookup"><span data-stu-id="0922c-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





