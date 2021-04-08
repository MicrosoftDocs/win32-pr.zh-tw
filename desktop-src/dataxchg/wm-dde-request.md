---
title: 'WM_DDE_REQUEST 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式會將 WM \_ DDE \_ 要求訊息張貼至 dde 伺服器應用程式，以要求資料項目的值。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685804"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="4dd9e-105">WM \_ DDE \_ 要求訊息</span><span class="sxs-lookup"><span data-stu-id="4dd9e-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="4dd9e-106">動態資料交換 (DDE) 用戶端應用程式會將 **WM \_ DDE \_ 要求** 訊息張貼至 dde 伺服器應用程式，以要求資料項目的值。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="4dd9e-107">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="4dd9e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4dd9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd9e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dd9e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd9e-110">傳送訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="4dd9e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dd9e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd9e-112">低序位字組指定標準或已註冊的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="4dd9e-113">高序位單字包含一個 atom，用來識別從伺服器要求的資料項目。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dd9e-114">備註</span><span class="sxs-lookup"><span data-stu-id="4dd9e-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="4dd9e-115">張貼</span><span class="sxs-lookup"><span data-stu-id="4dd9e-115">Posting</span></span>

<span data-ttu-id="4dd9e-116">用戶端應用程式會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="4dd9e-117">接收</span><span class="sxs-lookup"><span data-stu-id="4dd9e-117">Receiving</span></span>

<span data-ttu-id="4dd9e-118">如果接收 (伺服器) 應用程式可以滿足要求，它就會以包含所要求資料的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息進行回應。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="4dd9e-119">否則，它會以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息來回應。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="4dd9e-120">當回應 [**wm \_ dde \_ 資料**](wm-dde-data.md) 或 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息時，伺服器應用程式可以重複使用 atom，也可以刪除 atom 並建立一個新的 atom。</span><span class="sxs-lookup"><span data-stu-id="4dd9e-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd9e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dd9e-121">Requirements</span></span>



| <span data-ttu-id="4dd9e-122">需求</span><span class="sxs-lookup"><span data-stu-id="4dd9e-122">Requirement</span></span> | <span data-ttu-id="4dd9e-123">值</span><span class="sxs-lookup"><span data-stu-id="4dd9e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd9e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dd9e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd9e-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dd9e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4dd9e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dd9e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd9e-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dd9e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4dd9e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4dd9e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd9e-129"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="4dd9e-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd9e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dd9e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="4dd9e-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4dd9e-132">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="4dd9e-133">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="4dd9e-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="4dd9e-135">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="4dd9e-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="4dd9e-137">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="4dd9e-138">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="4dd9e-139">**WM \_ DDE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="4dd9e-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="4dd9e-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4dd9e-141">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="4dd9e-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

