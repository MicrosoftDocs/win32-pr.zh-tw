---
description: IScanProfileUI 介面可讓應用程式顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: 'IScanProfileUI 介面 (Scanprofileui .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001680"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="8f969-103">IScanProfileUI 介面</span><span class="sxs-lookup"><span data-stu-id="8f969-103">IScanProfileUI interface</span></span>

<span data-ttu-id="8f969-104">**IScanProfileUI** 介面可讓應用程式顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f969-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="8f969-105">成員</span><span class="sxs-lookup"><span data-stu-id="8f969-105">Members</span></span>

<span data-ttu-id="8f969-106">**IScanProfileUI** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="8f969-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8f969-107">**IScanProfileUI** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f969-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="8f969-108">方法</span><span class="sxs-lookup"><span data-stu-id="8f969-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8f969-109">方法</span><span class="sxs-lookup"><span data-stu-id="8f969-109">Methods</span></span>

<span data-ttu-id="8f969-110">**IScanProfileUI** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8f969-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="8f969-111">方法</span><span class="sxs-lookup"><span data-stu-id="8f969-111">Method</span></span>                                                             | <span data-ttu-id="8f969-112">描述</span><span class="sxs-lookup"><span data-stu-id="8f969-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f969-113">**ScanProfileDialog**</span><span class="sxs-lookup"><span data-stu-id="8f969-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="8f969-114">顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f969-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f969-115">備註</span><span class="sxs-lookup"><span data-stu-id="8f969-115">Remarks</span></span>

<span data-ttu-id="8f969-116">對話方塊為強制回應;在對話方塊關閉之前，使用者無法切換至父視窗。</span><span class="sxs-lookup"><span data-stu-id="8f969-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f969-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f969-117">Requirements</span></span>



| <span data-ttu-id="8f969-118">需求</span><span class="sxs-lookup"><span data-stu-id="8f969-118">Requirement</span></span> | <span data-ttu-id="8f969-119">值</span><span class="sxs-lookup"><span data-stu-id="8f969-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f969-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f969-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f969-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f969-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8f969-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f969-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f969-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f969-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f969-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8f969-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f969-125"><dt>Scanprofileui。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f969-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="8f969-126">Idl</span><span class="sxs-lookup"><span data-stu-id="8f969-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f969-127"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f969-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f969-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f969-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f969-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8f969-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="8f969-130">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="8f969-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
