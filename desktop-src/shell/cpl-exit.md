---
description: 先傳送一次至主控台應用程式的 CPlApplet 函式，再釋放包含主控台應用程式的 DLL。
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: 'CPL_EXIT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191179"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="3be24-103">CPL 結束 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="3be24-103">CPL\_EXIT message</span></span>

<span data-ttu-id="3be24-104">先傳送一次至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，再釋放包含主控台應用程式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="3be24-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="3be24-105">參數</span><span class="sxs-lookup"><span data-stu-id="3be24-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be24-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3be24-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3be24-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3be24-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3be24-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3be24-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3be24-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3be24-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be24-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3be24-110">Return value</span></span>

<span data-ttu-id="3be24-111">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="3be24-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be24-112">備註</span><span class="sxs-lookup"><span data-stu-id="3be24-112">Remarks</span></span>

<span data-ttu-id="3be24-113">這則訊息會在傳送最後一個 [**CPL \_ 停止**](cpl-stop.md) 訊息之後傳送。</span><span class="sxs-lookup"><span data-stu-id="3be24-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="3be24-114">為了回應這則訊息，主控台的應用程式必須釋放已配置的記憶體，並執行全域層級的清除。</span><span class="sxs-lookup"><span data-stu-id="3be24-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be24-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3be24-115">Requirements</span></span>



| <span data-ttu-id="3be24-116">需求</span><span class="sxs-lookup"><span data-stu-id="3be24-116">Requirement</span></span> | <span data-ttu-id="3be24-117">值</span><span class="sxs-lookup"><span data-stu-id="3be24-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3be24-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3be24-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3be24-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3be24-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3be24-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3be24-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3be24-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3be24-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3be24-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3be24-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be24-123"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3be24-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be24-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3be24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be24-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="3be24-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
