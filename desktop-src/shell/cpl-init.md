---
description: 傳送至主控台應用程式的 CPlApplet 函式，以提示它執行全域初始化（尤其是記憶體配置）。
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: 'CPL_INIT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972049"
---
# <a name="cpl_init-message"></a><span data-ttu-id="199e7-103">CPL \_ 初始訊息</span><span class="sxs-lookup"><span data-stu-id="199e7-103">CPL\_INIT message</span></span>

<span data-ttu-id="199e7-104">傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以提示它執行全域初始化（尤其是記憶體配置）。</span><span class="sxs-lookup"><span data-stu-id="199e7-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="199e7-105">參數</span><span class="sxs-lookup"><span data-stu-id="199e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199e7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="199e7-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="199e7-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="199e7-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="199e7-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="199e7-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="199e7-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="199e7-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199e7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="199e7-110">Return value</span></span>

<span data-ttu-id="199e7-111">如果初始化成功， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函數應該會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="199e7-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="199e7-112">否則，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="199e7-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="199e7-113">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 傳回零，控制應用程式就會結束通訊，並釋放包含主控台應用程式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="199e7-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="199e7-114">備註</span><span class="sxs-lookup"><span data-stu-id="199e7-114">Remarks</span></span>

<span data-ttu-id="199e7-115">因為這是主控台的應用程式可以表示錯誤狀況的唯一方法，所以應用程式應該配置記憶體以回應這則訊息。</span><span class="sxs-lookup"><span data-stu-id="199e7-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="199e7-116">在載入包含應用程式的 DLL 之後，會立即傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="199e7-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="199e7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="199e7-117">Requirements</span></span>



| <span data-ttu-id="199e7-118">需求</span><span class="sxs-lookup"><span data-stu-id="199e7-118">Requirement</span></span> | <span data-ttu-id="199e7-119">值</span><span class="sxs-lookup"><span data-stu-id="199e7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="199e7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="199e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="199e7-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="199e7-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="199e7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="199e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="199e7-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="199e7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="199e7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="199e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="199e7-125"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="199e7-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="199e7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="199e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199e7-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="199e7-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
