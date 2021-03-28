---
description: 通知您即將針對與隨附的 SMDATA 結構所指定之專案相關聯的燕號顯示資訊提示。
title: 'SMC_DISPLAYCHEVRONTIP 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469340"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="5b03b-103">SMC \_ DISPLAYCHEVRONTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="5b03b-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="5b03b-104">通知您即將針對與隨附的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定之專案相關聯的燕號顯示資訊提示。</span><span class="sxs-lookup"><span data-stu-id="5b03b-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="5b03b-105">參數</span><span class="sxs-lookup"><span data-stu-id="5b03b-105">Parameters</span></span>

<span data-ttu-id="5b03b-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5b03b-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b03b-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b03b-107">Return value</span></span>

<span data-ttu-id="5b03b-108">返回 \_ [確定] 以顯示提示。</span><span class="sxs-lookup"><span data-stu-id="5b03b-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="5b03b-109">傳回 \_ FALSE 以防止顯示提示。</span><span class="sxs-lookup"><span data-stu-id="5b03b-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b03b-110">備註</span><span class="sxs-lookup"><span data-stu-id="5b03b-110">Remarks</span></span>

<span data-ttu-id="5b03b-111">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="5b03b-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b03b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b03b-112">Requirements</span></span>



| <span data-ttu-id="5b03b-113">需求</span><span class="sxs-lookup"><span data-stu-id="5b03b-113">Requirement</span></span> | <span data-ttu-id="5b03b-114">值</span><span class="sxs-lookup"><span data-stu-id="5b03b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b03b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b03b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5b03b-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b03b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5b03b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b03b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5b03b-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b03b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b03b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5b03b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b03b-120"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b03b-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b03b-121">Idl</span><span class="sxs-lookup"><span data-stu-id="5b03b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b03b-122"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b03b-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




