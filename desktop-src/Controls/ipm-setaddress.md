---
title: 'IPM_SETADDRESS 訊息 (Commctrl .h) '
description: 在 IP 位址控制項中設定所有四個欄位的位址值。
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104465"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="27beb-104">IPM \_ SETADDRESS 訊息</span><span class="sxs-lookup"><span data-stu-id="27beb-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="27beb-105">在 IP 位址控制項中設定所有四個欄位的位址值。</span><span class="sxs-lookup"><span data-stu-id="27beb-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="27beb-106">參數</span><span class="sxs-lookup"><span data-stu-id="27beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27beb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27beb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="27beb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="27beb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="27beb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27beb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27beb-110">**DWORD** 值，包含新的位址。</span><span class="sxs-lookup"><span data-stu-id="27beb-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="27beb-111">欄位3值包含在位0到7。</span><span class="sxs-lookup"><span data-stu-id="27beb-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="27beb-112">欄位2值包含在位8到15之間。</span><span class="sxs-lookup"><span data-stu-id="27beb-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="27beb-113">欄位1值包含在位16到23之間。</span><span class="sxs-lookup"><span data-stu-id="27beb-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="27beb-114">欄位0值包含在位24到31之間。</span><span class="sxs-lookup"><span data-stu-id="27beb-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="27beb-115">[**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)宏也可以用來建立位址資訊。</span><span class="sxs-lookup"><span data-stu-id="27beb-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27beb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="27beb-116">Return value</span></span>

<span data-ttu-id="27beb-117">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="27beb-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="27beb-118">備註</span><span class="sxs-lookup"><span data-stu-id="27beb-118">Remarks</span></span>

<span data-ttu-id="27beb-119">此訊息不會產生 [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="27beb-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="27beb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="27beb-120">Requirements</span></span>



| <span data-ttu-id="27beb-121">需求</span><span class="sxs-lookup"><span data-stu-id="27beb-121">Requirement</span></span> | <span data-ttu-id="27beb-122">值</span><span class="sxs-lookup"><span data-stu-id="27beb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27beb-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27beb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27beb-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27beb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27beb-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27beb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27beb-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27beb-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27beb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="27beb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="27beb-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27beb-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





