---
title: 'TTM_GETTOOLINFO 訊息 (Commctrl .h) '
description: 抓取工具提示控制項維護的工具相關資訊。
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103733"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="aaf13-104">TTM \_ GETTOOLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="aaf13-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="aaf13-105">抓取工具提示控制項維護的工具相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aaf13-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaf13-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaf13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaf13-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aaf13-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="aaf13-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aaf13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaf13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf13-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aaf13-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="aaf13-111">傳送訊息時， **hwnd** 和 **uId** 成員會識別工具，而 **cbSize** 成員必須指定結構的大小。</span><span class="sxs-lookup"><span data-stu-id="aaf13-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="aaf13-112">使用此訊息抓取工具提示文字時，請確定 **TOOLINFO** 結構的 **lpszText** 成員指向 adquate 大小的有效緩衝區</span><span class="sxs-lookup"><span data-stu-id="aaf13-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf13-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaf13-113">Return value</span></span>

<span data-ttu-id="aaf13-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="aaf13-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf13-115">備註</span><span class="sxs-lookup"><span data-stu-id="aaf13-115">Remarks</span></span>

<span data-ttu-id="aaf13-116">如果工具提示控制項包含工具， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構會接收工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aaf13-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="aaf13-117">範例</span><span class="sxs-lookup"><span data-stu-id="aaf13-117">Examples</span></span>

<span data-ttu-id="aaf13-118">下列範例會重新置放工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="aaf13-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="aaf13-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaf13-119">Requirements</span></span>



| <span data-ttu-id="aaf13-120">需求</span><span class="sxs-lookup"><span data-stu-id="aaf13-120">Requirement</span></span> | <span data-ttu-id="aaf13-121">值</span><span class="sxs-lookup"><span data-stu-id="aaf13-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf13-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaf13-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf13-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaf13-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aaf13-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaf13-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf13-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaf13-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aaf13-126">標頭</span><span class="sxs-lookup"><span data-stu-id="aaf13-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaf13-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf13-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aaf13-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="aaf13-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aaf13-129">**TTM \_GETTOOLINFOW** (Unicode) 和 **TTM \_ GETTOOLINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="aaf13-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





