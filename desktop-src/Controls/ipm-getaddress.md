---
title: 'IPM_GETADDRESS 訊息 (Commctrl .h) '
description: 取得 IP 位址控制項中所有四個欄位的位址值。
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934632"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="33915-104">IPM \_ GETADDRESS 訊息</span><span class="sxs-lookup"><span data-stu-id="33915-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="33915-105">取得 IP 位址控制項中所有四個欄位的位址值。</span><span class="sxs-lookup"><span data-stu-id="33915-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="33915-106">參數</span><span class="sxs-lookup"><span data-stu-id="33915-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33915-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33915-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33915-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="33915-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33915-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33915-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33915-110">接收位址之 **DWORD** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="33915-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="33915-111">欄位3值會包含在位0到7。</span><span class="sxs-lookup"><span data-stu-id="33915-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="33915-112">欄位2值會包含在位8到15之間。</span><span class="sxs-lookup"><span data-stu-id="33915-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="33915-113">欄位1值會包含在位16到23之間。</span><span class="sxs-lookup"><span data-stu-id="33915-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="33915-114">欄位0值將包含在位24到31之間。</span><span class="sxs-lookup"><span data-stu-id="33915-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="33915-115">[**第一個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)、[**第二個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)、[**第三個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)和 [**第四個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress)宏也可以用來解壓縮位址資訊。</span><span class="sxs-lookup"><span data-stu-id="33915-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="33915-116">零會以任何空白欄位的位址傳回。</span><span class="sxs-lookup"><span data-stu-id="33915-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33915-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="33915-117">Return value</span></span>

<span data-ttu-id="33915-118">傳回非空白欄位的數目。</span><span class="sxs-lookup"><span data-stu-id="33915-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="33915-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="33915-119">Requirements</span></span>



| <span data-ttu-id="33915-120">需求</span><span class="sxs-lookup"><span data-stu-id="33915-120">Requirement</span></span> | <span data-ttu-id="33915-121">值</span><span class="sxs-lookup"><span data-stu-id="33915-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33915-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33915-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33915-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33915-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33915-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33915-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33915-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33915-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33915-126">標頭</span><span class="sxs-lookup"><span data-stu-id="33915-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33915-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33915-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





