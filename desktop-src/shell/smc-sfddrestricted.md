---
description: 要求是否可以將資料物件放在隨附 SMDATA 結構所指定的專案上。
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: 'SMC_SFDDRESTRICTED 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973445"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="76de5-103">SMC \_ SFDDRESTRICTED 訊息</span><span class="sxs-lookup"><span data-stu-id="76de5-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="76de5-104">要求是否可以將資料物件放在隨附 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案上。</span><span class="sxs-lookup"><span data-stu-id="76de5-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="76de5-105">參數</span><span class="sxs-lookup"><span data-stu-id="76de5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76de5-106">*pDropTarget*</span><span class="sxs-lookup"><span data-stu-id="76de5-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="76de5-107">Void 指標的位址，這個指標會接收 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="76de5-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="76de5-108">如果您不想要接受資料物件，請將此值設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="76de5-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76de5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="76de5-109">Return value</span></span>

<span data-ttu-id="76de5-110">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="76de5-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="76de5-111">備註</span><span class="sxs-lookup"><span data-stu-id="76de5-111">Remarks</span></span>

<span data-ttu-id="76de5-112">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="76de5-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="76de5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="76de5-113">Requirements</span></span>



| <span data-ttu-id="76de5-114">需求</span><span class="sxs-lookup"><span data-stu-id="76de5-114">Requirement</span></span> | <span data-ttu-id="76de5-115">值</span><span class="sxs-lookup"><span data-stu-id="76de5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76de5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76de5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="76de5-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76de5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="76de5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76de5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="76de5-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76de5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76de5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="76de5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="76de5-121"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="76de5-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="76de5-122">Idl</span><span class="sxs-lookup"><span data-stu-id="76de5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76de5-123"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="76de5-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
