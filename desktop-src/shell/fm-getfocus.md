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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841409"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="3109d-103">FM \_ GETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="3109d-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="3109d-104">由檔案管理員延伸模組傳送，以抓取具有輸入焦點的 [檔案管理員] 視窗類型。</span><span class="sxs-lookup"><span data-stu-id="3109d-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="3109d-105">參數</span><span class="sxs-lookup"><span data-stu-id="3109d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3109d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3109d-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3109d-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3109d-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3109d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3109d-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3109d-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3109d-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3109d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3109d-110">Return value</span></span>

<span data-ttu-id="3109d-111">傳回具有輸入焦點的 [檔案管理員] 視窗類型。</span><span class="sxs-lookup"><span data-stu-id="3109d-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="3109d-112">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="3109d-112">It can be one of the following values.</span></span>



| <span data-ttu-id="3109d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3109d-113">Return code</span></span>                                                                                    | <span data-ttu-id="3109d-114">描述</span><span class="sxs-lookup"><span data-stu-id="3109d-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="3109d-115"><dt>**FMFOCUS \_ 目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="3109d-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="3109d-116">目錄視窗的目錄部分。</span><span class="sxs-lookup"><span data-stu-id="3109d-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="3109d-117"><dt>**FMFOCUS \_ 樹狀結構**</dt></span><span class="sxs-lookup"><span data-stu-id="3109d-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="3109d-118">目錄視窗的樹狀結構部分。</span><span class="sxs-lookup"><span data-stu-id="3109d-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="3109d-119"><dt>**FMFOCUS \_ 磁片磁碟機**</dt></span><span class="sxs-lookup"><span data-stu-id="3109d-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="3109d-120">目錄視窗的磁片磁碟機列。</span><span class="sxs-lookup"><span data-stu-id="3109d-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="3109d-121"><dt>**FMFOCUS \_ 搜尋**</dt></span><span class="sxs-lookup"><span data-stu-id="3109d-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="3109d-122">搜尋結果視窗。</span><span class="sxs-lookup"><span data-stu-id="3109d-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="3109d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3109d-123">Requirements</span></span>



| <span data-ttu-id="3109d-124">需求</span><span class="sxs-lookup"><span data-stu-id="3109d-124">Requirement</span></span> | <span data-ttu-id="3109d-125">值</span><span class="sxs-lookup"><span data-stu-id="3109d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3109d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3109d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3109d-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3109d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3109d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3109d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3109d-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3109d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3109d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3109d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3109d-131"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="3109d-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




