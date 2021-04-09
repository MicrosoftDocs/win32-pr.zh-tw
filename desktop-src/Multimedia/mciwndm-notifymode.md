---
title: 'MCIWNDM_NOTIFYMODE 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYMODE 訊息會通知應用程式的父視窗，該應用程式的 MCI 裝置操作模式已變更。
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024562"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="743e9-104">MCIWNDM \_ NOTIFYMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="743e9-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="743e9-105">**MCIWNDM \_ NOTIFYMODE** 訊息會通知應用程式的父視窗，該應用程式的 MCI 裝置操作模式已變更。</span><span class="sxs-lookup"><span data-stu-id="743e9-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="743e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="743e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743e9-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="743e9-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="743e9-108">MCIWnd 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="743e9-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="743e9-109"><span id="mode"></span><span id="MODE"></span>*模式*</span><span class="sxs-lookup"><span data-stu-id="743e9-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="743e9-110">對應至 MCI 模式的整數。</span><span class="sxs-lookup"><span data-stu-id="743e9-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="743e9-111">備註</span><span class="sxs-lookup"><span data-stu-id="743e9-111">Remarks</span></span>

<span data-ttu-id="743e9-112">您可以藉由指定 [MCIWNDF \_ NOTIFYMODE] 視窗樣式，來啟用 MCI 裝置之模式變更的通知。</span><span class="sxs-lookup"><span data-stu-id="743e9-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="743e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="743e9-113">Requirements</span></span>



| <span data-ttu-id="743e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="743e9-114">Requirement</span></span> | <span data-ttu-id="743e9-115">值</span><span class="sxs-lookup"><span data-stu-id="743e9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="743e9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="743e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="743e9-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="743e9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="743e9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="743e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="743e9-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="743e9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="743e9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="743e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="743e9-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="743e9-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





