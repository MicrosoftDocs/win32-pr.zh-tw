---
title: 'TF_LBMENUF_ 常數 (Ctfutb) '
description: TF \_ LBMENUF \_ \ 常數是在 ITfMenu AddMenuItem 方法中用來指定語言列中功能表項目的特性。
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934330"
---
# <a name="tf_lbmenuf_-constants"></a><span data-ttu-id="65bf7-103">TF \_ LBMENUF \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="65bf7-103">TF\_LBMENUF\_\* Constants</span></span>

<span data-ttu-id="65bf7-104">在 [ITfMenu：： AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)方法中，會使用 \**TF \_ \_ \* LBMENUF* _ 常數來指定語言列中功能表項目的特性。</span><span class="sxs-lookup"><span data-stu-id="65bf7-104">The \**TF\_LBMENUF\_\** _ constants are used in the [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) method to specify the characteristics of a menu item in the language bar.</span></span>



| <span data-ttu-id="65bf7-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="65bf7-105">Constant/value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="65bf7-106">Description</span><span class="sxs-lookup"><span data-stu-id="65bf7-106">Description</span></span>                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <span data-ttu-id="65bf7-107"><dt>_ \* TF \_LBMENUF \_ CHECKED \* \*</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-107"><dt>_\*TF\_LBMENUF\_CHECKED\*\*</dt> <dt>0x01</dt></span></span> </dl>                | <span data-ttu-id="65bf7-108">已核取功能表項目。</span><span class="sxs-lookup"><span data-stu-id="65bf7-108">The menu item is checked.</span></span><br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <span data-ttu-id="65bf7-109"><dt>**TF \_LBMENUF \_ 子功能表**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-109"><dt>**TF\_LBMENUF\_SUBMENU**</dt> <dt>0x02</dt></span></span> </dl>                | <span data-ttu-id="65bf7-110">功能表項目是子功能表。</span><span class="sxs-lookup"><span data-stu-id="65bf7-110">The menu item is a submenu.</span></span><br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <span data-ttu-id="65bf7-111"><dt>**TF \_LBMENUF \_ 分隔符號**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-111"><dt>**TF\_LBMENUF\_SEPARATOR**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="65bf7-112">功能表項目為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="65bf7-112">The menu item is a separator.</span></span><br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <span data-ttu-id="65bf7-113"><dt>**TF \_LBMENUF \_ RADIOCHECKED**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-113"><dt>**TF\_LBMENUF\_RADIOCHECKED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="65bf7-114">功能表項目是一個單選標記。</span><span class="sxs-lookup"><span data-stu-id="65bf7-114">The menu item is a radio check mark.</span></span><br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <span data-ttu-id="65bf7-115"><dt>**TF \_LBMENUF \_ 灰色**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-115"><dt>**TF\_LBMENUF\_GRAYED**</dt> <dt>0x10</dt></span></span> </dl>                   | <span data-ttu-id="65bf7-116">功能表項目已停用。</span><span class="sxs-lookup"><span data-stu-id="65bf7-116">The menu item is disabled.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="65bf7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="65bf7-117">Requirements</span></span>



| <span data-ttu-id="65bf7-118">需求</span><span class="sxs-lookup"><span data-stu-id="65bf7-118">Requirement</span></span> | <span data-ttu-id="65bf7-119">值</span><span class="sxs-lookup"><span data-stu-id="65bf7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65bf7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65bf7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65bf7-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65bf7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="65bf7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65bf7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65bf7-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65bf7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65bf7-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="65bf7-124">Redistributable</span></span><br/>          | <span data-ttu-id="65bf7-125">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="65bf7-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="65bf7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="65bf7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65bf7-127"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="65bf7-128">Idl</span><span class="sxs-lookup"><span data-stu-id="65bf7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65bf7-129"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="65bf7-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65bf7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65bf7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65bf7-131">ITfMenu::AddMenuItem</span><span class="sxs-lookup"><span data-stu-id="65bf7-131">ITfMenu::AddMenuItem</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 





