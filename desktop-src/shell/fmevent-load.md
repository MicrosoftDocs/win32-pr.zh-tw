---
description: 當檔案管理員載入 DLL 時，傳送至擴充 DLL。
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: 'FMEVENT_LOAD 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973225"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="46900-103">FMEVENT \_ 載入訊息</span><span class="sxs-lookup"><span data-stu-id="46900-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="46900-104">當檔案管理員載入 DLL 時，傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="46900-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="46900-105">參數</span><span class="sxs-lookup"><span data-stu-id="46900-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46900-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46900-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46900-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="46900-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="46900-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="46900-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="46900-109">[**FMS \_ 載入**](fms-load.md)結構的位址，指定功能表項目差異值。</span><span class="sxs-lookup"><span data-stu-id="46900-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46900-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="46900-110">Return value</span></span>

<span data-ttu-id="46900-111">延伸模組 DLL 必須傳回 **TRUE** ，才能繼續載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="46900-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="46900-112">如果 DLL 傳回 **FALSE**，則 [檔案管理員] 會呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式，並結束與延伸模組 DLL 的任何通訊。</span><span class="sxs-lookup"><span data-stu-id="46900-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="46900-113">備註</span><span class="sxs-lookup"><span data-stu-id="46900-113">Remarks</span></span>

<span data-ttu-id="46900-114">應用程式應該填滿 [**FMS \_ 載入**](fms-load.md)結構中的 **DwSize**、 **szMenuName** 和 **hMenu** 成員。</span><span class="sxs-lookup"><span data-stu-id="46900-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="46900-115">它也應該儲存 **wMenuDelta** 成員的值，並在修改功能表時使用它來識別功能表項目。</span><span class="sxs-lookup"><span data-stu-id="46900-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="46900-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="46900-116">Requirements</span></span>



| <span data-ttu-id="46900-117">需求</span><span class="sxs-lookup"><span data-stu-id="46900-117">Requirement</span></span> | <span data-ttu-id="46900-118">值</span><span class="sxs-lookup"><span data-stu-id="46900-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46900-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46900-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46900-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46900-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="46900-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46900-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46900-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46900-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46900-123">標頭</span><span class="sxs-lookup"><span data-stu-id="46900-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46900-124"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="46900-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46900-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46900-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46900-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="46900-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
