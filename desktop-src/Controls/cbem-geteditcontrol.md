---
title: 'CBEM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 取得 ComboBoxEx 控制項之編輯控制項部分的控制碼。 當 ComboBoxEx 控制項設定為 CBS 下拉式樣式時，會使用編輯方塊 \_ 。
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105599"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="a3c44-105">CBEM \_ GETEDITCONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="a3c44-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="a3c44-106">取得 ComboBoxEx 控制項之編輯控制項部分的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a3c44-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="a3c44-107">當 ComboBoxEx 控制項設定為 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式時，會使用編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="a3c44-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3c44-108">參數</span><span class="sxs-lookup"><span data-stu-id="a3c44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3c44-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a3c44-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a3c44-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a3c44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3c44-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a3c44-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a3c44-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c44-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3c44-113">Return value</span></span>

<span data-ttu-id="a3c44-114">傳回 ComboBoxEx 控制項中編輯控制項的控制碼（如果它使用 [**CBS \_ 下拉式清單**](combo-box-styles.md) 樣式）。</span><span class="sxs-lookup"><span data-stu-id="a3c44-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="a3c44-115">否則，訊息會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a3c44-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c44-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3c44-116">Requirements</span></span>



| <span data-ttu-id="a3c44-117">需求</span><span class="sxs-lookup"><span data-stu-id="a3c44-117">Requirement</span></span> | <span data-ttu-id="a3c44-118">值</span><span class="sxs-lookup"><span data-stu-id="a3c44-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c44-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3c44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c44-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3c44-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3c44-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3c44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c44-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3c44-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3c44-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a3c44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c44-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c44-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





