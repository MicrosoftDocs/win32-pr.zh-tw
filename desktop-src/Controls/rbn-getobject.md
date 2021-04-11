---
title: 'RBN_GETOBJECT (Commctrl 的通知碼) '
description: '\_當物件拖曳至控制項中的範圍時，以 RBS REGISTERDROP 樣式建立的 Rebar 控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104777"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="79354-105">RBN \_ GETOBJECT 通知碼</span><span class="sxs-lookup"><span data-stu-id="79354-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="79354-106">當物件拖曳至控制項中的範圍時，以 [**RBS \_ REGISTERDROP**](rebar-control-styles.md) 樣式建立的 Rebar 控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="79354-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="79354-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="79354-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="79354-108">參數</span><span class="sxs-lookup"><span data-stu-id="79354-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79354-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79354-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79354-110">[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含將物件拖曳到其中的頻外相關資訊，同時也會接收接收應用程式提供的資料，以回應此通知碼。</span><span class="sxs-lookup"><span data-stu-id="79354-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79354-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="79354-111">Return value</span></span>

<span data-ttu-id="79354-112">此通知碼的傳回值必須為零。</span><span class="sxs-lookup"><span data-stu-id="79354-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="79354-113">備註</span><span class="sxs-lookup"><span data-stu-id="79354-113">Remarks</span></span>

<span data-ttu-id="79354-114">若要接收 RBN 的 \_ GETOBJECT 通知碼，請呼叫 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) 或 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)來初始化 OLE。</span><span class="sxs-lookup"><span data-stu-id="79354-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="79354-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="79354-115">Requirements</span></span>



| <span data-ttu-id="79354-116">需求</span><span class="sxs-lookup"><span data-stu-id="79354-116">Requirement</span></span> | <span data-ttu-id="79354-117">值</span><span class="sxs-lookup"><span data-stu-id="79354-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79354-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79354-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79354-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79354-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79354-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79354-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79354-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79354-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79354-122">標頭</span><span class="sxs-lookup"><span data-stu-id="79354-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79354-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="79354-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

