---
description: 傳回伴隨的 SMDATA 結構所指定之專案的預設圖示。
title: 'SMC_DEFAULTICON 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991650"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="004f1-103">SMC \_ DEFAULTICON 訊息</span><span class="sxs-lookup"><span data-stu-id="004f1-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="004f1-104">傳回伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定之專案的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="004f1-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="004f1-105">參數</span><span class="sxs-lookup"><span data-stu-id="004f1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004f1-106">*pwszIcon*</span><span class="sxs-lookup"><span data-stu-id="004f1-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="004f1-107">字串的指標，該字串會接收包含預設圖示之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="004f1-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="004f1-108">*圖示*</span><span class="sxs-lookup"><span data-stu-id="004f1-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="004f1-109">整數的指標，該整數會在 *pwszIcon* 所指定的檔案中接收圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="004f1-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004f1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="004f1-110">Return value</span></span>

<span data-ttu-id="004f1-111">返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="004f1-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="004f1-112">備註</span><span class="sxs-lookup"><span data-stu-id="004f1-112">Remarks</span></span>

<span data-ttu-id="004f1-113">此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。</span><span class="sxs-lookup"><span data-stu-id="004f1-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="004f1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="004f1-114">Requirements</span></span>



| <span data-ttu-id="004f1-115">需求</span><span class="sxs-lookup"><span data-stu-id="004f1-115">Requirement</span></span> | <span data-ttu-id="004f1-116">值</span><span class="sxs-lookup"><span data-stu-id="004f1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="004f1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="004f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="004f1-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="004f1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="004f1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="004f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="004f1-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="004f1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="004f1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="004f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="004f1-122"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="004f1-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="004f1-123">Idl</span><span class="sxs-lookup"><span data-stu-id="004f1-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="004f1-124"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="004f1-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




