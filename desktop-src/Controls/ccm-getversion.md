---
title: 'CCM_GETVERSION 訊息 (Commctrl .h) '
description: 取得最新的 CCM SETVERSION 訊息之控制項集的版本號碼 \_ 。
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104513"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="ed049-104">CCM \_ GETVERSION 訊息</span><span class="sxs-lookup"><span data-stu-id="ed049-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="ed049-105">取得最新的 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息之控制項集的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ed049-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed049-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed049-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed049-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ed049-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ed049-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ed049-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed049-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ed049-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ed049-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed049-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed049-111">Return value</span></span>

<span data-ttu-id="ed049-112">傳回最新的 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息所設定的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ed049-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="ed049-113">如果沒有傳送這類訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ed049-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed049-114">備註</span><span class="sxs-lookup"><span data-stu-id="ed049-114">Remarks</span></span>

<span data-ttu-id="ed049-115">此訊息不會傳回 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="ed049-115">This message does not return the DLL version.</span></span> <span data-ttu-id="ed049-116">請參閱 [Shell 版本](common-control-versions.md) ，以取得如何使用 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 來取得目前 DLL 版本的討論。</span><span class="sxs-lookup"><span data-stu-id="ed049-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="ed049-117">版本號碼是以控制項為基礎設定的，而且所有控制項都可能不相同。</span><span class="sxs-lookup"><span data-stu-id="ed049-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ed049-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed049-118">Requirements</span></span>



| <span data-ttu-id="ed049-119">需求</span><span class="sxs-lookup"><span data-stu-id="ed049-119">Requirement</span></span> | <span data-ttu-id="ed049-120">值</span><span class="sxs-lookup"><span data-stu-id="ed049-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed049-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed049-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed049-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed049-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed049-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed049-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed049-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed049-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed049-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ed049-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed049-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed049-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

