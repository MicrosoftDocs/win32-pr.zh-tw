---
description: 當檔案管理員載入其工具列時，傳送至擴充 DLL。 此訊息可讓延伸模組 DLL 將按鈕新增至 [檔案管理員] 工具列。
title: 'FMEVENT_TOOLBARLOAD 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192698"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="63600-104">FMEVENT \_ TOOLBARLOAD 訊息</span><span class="sxs-lookup"><span data-stu-id="63600-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="63600-105">當檔案管理員載入其工具列時，傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="63600-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="63600-106">此訊息可讓延伸模組 DLL 將按鈕新增至 [檔案管理員] 工具列。</span><span class="sxs-lookup"><span data-stu-id="63600-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="63600-107">參數</span><span class="sxs-lookup"><span data-stu-id="63600-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63600-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63600-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="63600-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="63600-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="63600-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="63600-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="63600-111">[**FMS \_ TOOLBARLOAD**](fms-toolbarload.md)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="63600-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="63600-112">如果延伸模組 DLL 將按鈕新增至 [檔案管理員] 中的工具列，則 DLL 應以按鈕的相關資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="63600-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63600-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="63600-113">Return value</span></span>

<span data-ttu-id="63600-114">延伸模組 DLL 必須傳回 **TRUE** ，才能將按鈕加入至工具列。</span><span class="sxs-lookup"><span data-stu-id="63600-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="63600-115">如果 DLL 傳回 **FALSE**，則 [檔案管理員] 不會加入按鈕。</span><span class="sxs-lookup"><span data-stu-id="63600-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="63600-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="63600-116">Requirements</span></span>



| <span data-ttu-id="63600-117">需求</span><span class="sxs-lookup"><span data-stu-id="63600-117">Requirement</span></span> | <span data-ttu-id="63600-118">值</span><span class="sxs-lookup"><span data-stu-id="63600-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63600-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63600-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63600-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63600-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="63600-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63600-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63600-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63600-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63600-123">標頭</span><span class="sxs-lookup"><span data-stu-id="63600-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63600-124"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="63600-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63600-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63600-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63600-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="63600-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




