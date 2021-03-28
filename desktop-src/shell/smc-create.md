---
description: 通知您已建立功能表區。
title: 'SMC_CREATE 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991655"
---
# <a name="smc_create-message"></a><span data-ttu-id="b6aa1-103">SMC \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="b6aa1-103">SMC\_CREATE message</span></span>

<span data-ttu-id="b6aa1-104">通知您已建立功能表區。</span><span class="sxs-lookup"><span data-stu-id="b6aa1-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="b6aa1-105">參數</span><span class="sxs-lookup"><span data-stu-id="b6aa1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6aa1-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="b6aa1-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="b6aa1-107">[**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata)結構的 **pvUserData** 成員指標。</span><span class="sxs-lookup"><span data-stu-id="b6aa1-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6aa1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6aa1-108">Return value</span></span>

<span data-ttu-id="b6aa1-109">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="b6aa1-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6aa1-110">備註</span><span class="sxs-lookup"><span data-stu-id="b6aa1-110">Remarks</span></span>

<span data-ttu-id="b6aa1-111">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="b6aa1-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6aa1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6aa1-112">Requirements</span></span>



| <span data-ttu-id="b6aa1-113">需求</span><span class="sxs-lookup"><span data-stu-id="b6aa1-113">Requirement</span></span> | <span data-ttu-id="b6aa1-114">值</span><span class="sxs-lookup"><span data-stu-id="b6aa1-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6aa1-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6aa1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6aa1-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6aa1-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6aa1-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6aa1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6aa1-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6aa1-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6aa1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b6aa1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6aa1-120"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6aa1-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6aa1-121">Idl</span><span class="sxs-lookup"><span data-stu-id="b6aa1-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6aa1-122"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6aa1-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




