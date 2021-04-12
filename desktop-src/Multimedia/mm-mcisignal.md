---
title: 'MM_MCISIGNAL 訊息 (Mmsystem .h) '
description: MM \_ MCISIGNAL 訊息會傳送至視窗，以通知應用程式 mci 裝置已達先前的信號 ( MCI 信號) 命令中所定義的位置 \_ 。
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385021"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="93548-104">MM \_ MCISIGNAL 訊息</span><span class="sxs-lookup"><span data-stu-id="93548-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="93548-105">**MM \_ MCISIGNAL** 訊息會傳送至視窗，以通知應用程式 mci 裝置已達先前的 [**信號**](signal.md) ( [**MCI \_ 信號**](mci-signal.md)) 命令中所定義的位置。</span><span class="sxs-lookup"><span data-stu-id="93548-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="93548-106">參數</span><span class="sxs-lookup"><span data-stu-id="93548-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93548-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*</span><span class="sxs-lookup"><span data-stu-id="93548-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="93548-108">起始信號訊息之裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93548-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="93548-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span><span class="sxs-lookup"><span data-stu-id="93548-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="93548-110">當 **信號** 命令已定義此回呼函式時，會在 **MCI \_ DGV \_ 信號 \_ PARAMS** 結構的 **dwUserParm** 成員中傳遞值。</span><span class="sxs-lookup"><span data-stu-id="93548-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="93548-111">或者，它可能會包含位置值。</span><span class="sxs-lookup"><span data-stu-id="93548-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93548-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="93548-112">Requirements</span></span>



| <span data-ttu-id="93548-113">需求</span><span class="sxs-lookup"><span data-stu-id="93548-113">Requirement</span></span> | <span data-ttu-id="93548-114">值</span><span class="sxs-lookup"><span data-stu-id="93548-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93548-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93548-115">Minimum supported client</span></span><br/> | <span data-ttu-id="93548-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93548-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93548-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93548-117">Minimum supported server</span></span><br/> | <span data-ttu-id="93548-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93548-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93548-119">標頭</span><span class="sxs-lookup"><span data-stu-id="93548-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="93548-120"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="93548-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93548-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93548-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93548-122">Mci</span><span class="sxs-lookup"><span data-stu-id="93548-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="93548-123">MCI 訊息</span><span class="sxs-lookup"><span data-stu-id="93548-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="93548-124">**signal**</span><span class="sxs-lookup"><span data-stu-id="93548-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





