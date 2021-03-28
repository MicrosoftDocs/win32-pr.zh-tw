---
description: 由檔案管理員延伸模組傳送，以抓取具有輸入焦點的 [檔案管理員] 視窗類型。
title: 'FM_GETFOCUS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973240"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="50692-103">FM \_ GETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="50692-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="50692-104">由檔案管理員延伸模組傳送，以抓取具有輸入焦點的 [檔案管理員] 視窗類型。</span><span class="sxs-lookup"><span data-stu-id="50692-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="50692-105">參數</span><span class="sxs-lookup"><span data-stu-id="50692-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50692-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50692-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50692-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="50692-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50692-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50692-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="50692-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="50692-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50692-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="50692-110">Return value</span></span>

<span data-ttu-id="50692-111">傳回具有輸入焦點的 [檔案管理員] 視窗類型。</span><span class="sxs-lookup"><span data-stu-id="50692-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="50692-112">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="50692-112">It can be one of the following values.</span></span>



| <span data-ttu-id="50692-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="50692-113">Return code</span></span>                                                                                    | <span data-ttu-id="50692-114">Description</span><span class="sxs-lookup"><span data-stu-id="50692-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="50692-115"><dt>**FMFOCUS \_ 目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="50692-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="50692-116">目錄視窗的目錄部分。</span><span class="sxs-lookup"><span data-stu-id="50692-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="50692-117"><dt>**FMFOCUS \_ 樹狀結構**</dt></span><span class="sxs-lookup"><span data-stu-id="50692-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="50692-118">目錄視窗的樹狀結構部分。</span><span class="sxs-lookup"><span data-stu-id="50692-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="50692-119"><dt>**FMFOCUS \_ 磁片磁碟機**</dt></span><span class="sxs-lookup"><span data-stu-id="50692-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="50692-120">目錄視窗的磁片磁碟機列。</span><span class="sxs-lookup"><span data-stu-id="50692-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="50692-121"><dt>**FMFOCUS \_ 搜尋**</dt></span><span class="sxs-lookup"><span data-stu-id="50692-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="50692-122">搜尋結果視窗。</span><span class="sxs-lookup"><span data-stu-id="50692-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="50692-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="50692-123">Requirements</span></span>



| <span data-ttu-id="50692-124">需求</span><span class="sxs-lookup"><span data-stu-id="50692-124">Requirement</span></span> | <span data-ttu-id="50692-125">值</span><span class="sxs-lookup"><span data-stu-id="50692-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50692-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50692-126">Minimum supported client</span></span><br/> | <span data-ttu-id="50692-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50692-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="50692-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50692-128">Minimum supported server</span></span><br/> | <span data-ttu-id="50692-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50692-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50692-130">標頭</span><span class="sxs-lookup"><span data-stu-id="50692-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="50692-131"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="50692-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




