---
title: 'TB_GETSTATE 訊息 (Commctrl .h) '
description: 抓取工具列中指定之按鈕的狀態相關資訊，例如是否已啟用、已按下或已核取。
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843247"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="35335-104">TB \_ >getstate 訊息</span><span class="sxs-lookup"><span data-stu-id="35335-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="35335-105">抓取工具列中指定之按鈕的狀態相關資訊，例如是否已啟用、已按下或已核取。</span><span class="sxs-lookup"><span data-stu-id="35335-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="35335-106">參數</span><span class="sxs-lookup"><span data-stu-id="35335-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35335-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35335-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35335-108">要取得其資訊之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="35335-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="35335-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35335-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="35335-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="35335-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35335-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="35335-111">Return value</span></span>

<span data-ttu-id="35335-112">如果成功，則傳回按鈕狀態資訊，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="35335-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="35335-113">按鈕狀態資訊可以是 [ [**工具列按鈕狀態**](toolbar-button-states.md)] 中所列的值組合。</span><span class="sxs-lookup"><span data-stu-id="35335-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35335-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="35335-114">Requirements</span></span>



| <span data-ttu-id="35335-115">需求</span><span class="sxs-lookup"><span data-stu-id="35335-115">Requirement</span></span> | <span data-ttu-id="35335-116">值</span><span class="sxs-lookup"><span data-stu-id="35335-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35335-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35335-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35335-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35335-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35335-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35335-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35335-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35335-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35335-121">標頭</span><span class="sxs-lookup"><span data-stu-id="35335-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35335-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="35335-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





