---
description: 子類別中的所有控制項，以及對話方塊視窗本身的子類別。
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001167"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="2b75a-103">Ctl3dSubclassDlgEx 函式</span><span class="sxs-lookup"><span data-stu-id="2b75a-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="2b75a-104">子類別中的所有控制項，以及對話方塊視窗本身的子類別。</span><span class="sxs-lookup"><span data-stu-id="2b75a-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b75a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b75a-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="2b75a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b75a-107">*hwndDlg*</span><span class="sxs-lookup"><span data-stu-id="2b75a-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="2b75a-108">對話方塊視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2b75a-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="2b75a-109">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2b75a-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="2b75a-110">要子類別化的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="2b75a-110">The control types to be subclassed.</span></span> <span data-ttu-id="2b75a-111">這個值可以是下列任何一項。</span><span class="sxs-lookup"><span data-stu-id="2b75a-111">This value can be any of the following.</span></span>



| <span data-ttu-id="2b75a-112">值</span><span class="sxs-lookup"><span data-stu-id="2b75a-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="2b75a-113">意義</span><span class="sxs-lookup"><span data-stu-id="2b75a-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="2b75a-114"><dt>**CTL3D \_按鈕**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="2b75a-115">子類別按鈕。</span><span class="sxs-lookup"><span data-stu-id="2b75a-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="2b75a-116"><dt>**CTL3D \_清單方塊**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="2b75a-117">子類別清單方塊。</span><span class="sxs-lookup"><span data-stu-id="2b75a-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="2b75a-118"><dt>**CTL3D \_編輯**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="2b75a-119">子類別編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="2b75a-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="2b75a-120"><dt>**CTL3D \_COMBOS**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="2b75a-121">子類別下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="2b75a-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="2b75a-122"><dt>**CTL3D \_STATICTEXTS**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="2b75a-123">子類別靜態文字控制項。</span><span class="sxs-lookup"><span data-stu-id="2b75a-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="2b75a-124"><dt>**CTL3D \_STATICFRAMES**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="2b75a-125">子類別靜態框架。</span><span class="sxs-lookup"><span data-stu-id="2b75a-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="2b75a-126"><dt>**CTL3D \_所有**</dt> <dt>0xffff</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="2b75a-127">將所有控制項子類別化。</span><span class="sxs-lookup"><span data-stu-id="2b75a-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="2b75a-128"><dt>**CTL3D \_NODLGWINDOW**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="2b75a-129">請勿將交談視窗子類別化。</span><span class="sxs-lookup"><span data-stu-id="2b75a-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b75a-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b75a-130">Return value</span></span>

<span data-ttu-id="2b75a-131">如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2b75a-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b75a-132">備註</span><span class="sxs-lookup"><span data-stu-id="2b75a-132">Remarks</span></span>

<span data-ttu-id="2b75a-133">此函數在以 c + + 為基礎的應用程式中特別有用。</span><span class="sxs-lookup"><span data-stu-id="2b75a-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="2b75a-134">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="2b75a-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b75a-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b75a-135">Requirements</span></span>



| <span data-ttu-id="2b75a-136">需求</span><span class="sxs-lookup"><span data-stu-id="2b75a-136">Requirement</span></span> | <span data-ttu-id="2b75a-137">值</span><span class="sxs-lookup"><span data-stu-id="2b75a-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b75a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2b75a-138">DLL</span></span><br/> | <dl> <span data-ttu-id="2b75a-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
