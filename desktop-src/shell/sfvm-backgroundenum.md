---
description: 允許回呼物件在背景執行緒上要求列舉。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_BACKGROUNDENUM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991683"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="c0645-104">SFVM \_ BACKGROUNDENUM 訊息</span><span class="sxs-lookup"><span data-stu-id="c0645-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="c0645-105">允許回呼物件在背景執行緒上要求列舉。</span><span class="sxs-lookup"><span data-stu-id="c0645-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="c0645-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="c0645-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="c0645-107">參數</span><span class="sxs-lookup"><span data-stu-id="c0645-107">Parameters</span></span>

<span data-ttu-id="c0645-108">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0645-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0645-109">備註</span><span class="sxs-lookup"><span data-stu-id="c0645-109">Remarks</span></span>

<span data-ttu-id="c0645-110">回應此通知時，請返回 \_ [確定] 以啟用背景列舉。</span><span class="sxs-lookup"><span data-stu-id="c0645-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="c0645-111">根據預設，系統資料夾物件將會在列舉進行時顯示「停止顯示」動畫。</span><span class="sxs-lookup"><span data-stu-id="c0645-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="c0645-112">若要指定自訂動畫，請處理 [**SFVM \_ GETANIMATION**](sfvm-getanimation.md)。</span><span class="sxs-lookup"><span data-stu-id="c0645-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0645-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0645-113">Requirements</span></span>



| <span data-ttu-id="c0645-114">需求</span><span class="sxs-lookup"><span data-stu-id="c0645-114">Requirement</span></span> | <span data-ttu-id="c0645-115">值</span><span class="sxs-lookup"><span data-stu-id="c0645-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0645-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0645-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0645-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0645-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0645-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0645-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0645-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0645-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0645-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c0645-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0645-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0645-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
