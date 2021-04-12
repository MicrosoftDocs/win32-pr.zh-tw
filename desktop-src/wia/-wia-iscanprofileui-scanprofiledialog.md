---
description: 顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI：： ScanProfileDialog 方法 (Scanprofileui .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192795"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="65f67-103">IScanProfileUI：： ScanProfileDialog 方法</span><span class="sxs-lookup"><span data-stu-id="65f67-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="65f67-104">顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="65f67-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f67-105">語法</span><span class="sxs-lookup"><span data-stu-id="65f67-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="65f67-106">參數</span><span class="sxs-lookup"><span data-stu-id="65f67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f67-107">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65f67-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f67-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="65f67-108">Type: **HWND**</span></span>

<span data-ttu-id="65f67-109">擁有對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="65f67-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f67-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="65f67-110">Return value</span></span>

<span data-ttu-id="65f67-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65f67-111">Type: **HRESULT**</span></span>

<span data-ttu-id="65f67-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="65f67-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65f67-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65f67-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f67-114">備註</span><span class="sxs-lookup"><span data-stu-id="65f67-114">Remarks</span></span>

<span data-ttu-id="65f67-115">對話方塊為強制回應;在對話方塊關閉之前，使用者無法切換至父視窗。</span><span class="sxs-lookup"><span data-stu-id="65f67-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="65f67-116">您 `<ProfileName>` `<WiaItem>` 可以在對話方塊中變更元素和元素的值。</span><span class="sxs-lookup"><span data-stu-id="65f67-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="65f67-117">您 `<Default>` 可以新增或刪除元素。</span><span class="sxs-lookup"><span data-stu-id="65f67-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="65f67-118">您無法在對話方塊中進行掃描設定檔的其他變更。</span><span class="sxs-lookup"><span data-stu-id="65f67-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f67-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="65f67-119">Requirements</span></span>



| <span data-ttu-id="65f67-120">需求</span><span class="sxs-lookup"><span data-stu-id="65f67-120">Requirement</span></span> | <span data-ttu-id="65f67-121">值</span><span class="sxs-lookup"><span data-stu-id="65f67-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f67-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65f67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="65f67-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65f67-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="65f67-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65f67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="65f67-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65f67-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65f67-126">標頭</span><span class="sxs-lookup"><span data-stu-id="65f67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f67-127"><dt>Scanprofileui。h</dt></span><span class="sxs-lookup"><span data-stu-id="65f67-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="65f67-128">Idl</span><span class="sxs-lookup"><span data-stu-id="65f67-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65f67-129"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="65f67-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f67-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65f67-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f67-131">**IScanProfileUI**</span><span class="sxs-lookup"><span data-stu-id="65f67-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="65f67-132">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="65f67-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




