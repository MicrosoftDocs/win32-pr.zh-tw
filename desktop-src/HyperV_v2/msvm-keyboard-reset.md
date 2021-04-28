---
description: 重設 Msvm_Keyboard 類別的方法-重設虛擬鍵盤。
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Msvm_Keyboard 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 14c3166ce57fab4693dec87d3d81a55f1f688aa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111706"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="9a511-103">Msvm 鍵盤類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9a511-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="9a511-104">重設虛擬鍵盤。</span><span class="sxs-lookup"><span data-stu-id="9a511-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a511-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a511-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="9a511-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a511-106">Parameters</span></span>

<span data-ttu-id="9a511-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9a511-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a511-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a511-108">Return value</span></span>

<span data-ttu-id="9a511-109">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="9a511-109">A return value of zero indicates success.</span></span> <span data-ttu-id="9a511-110">傳回值為1表示失敗，因為不支援此方法。</span><span class="sxs-lookup"><span data-stu-id="9a511-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="9a511-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9a511-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9a511-112">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="9a511-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9a511-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a511-113">Requirements</span></span>



| <span data-ttu-id="9a511-114">需求</span><span class="sxs-lookup"><span data-stu-id="9a511-114">Requirement</span></span> | <span data-ttu-id="9a511-115">值</span><span class="sxs-lookup"><span data-stu-id="9a511-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a511-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a511-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a511-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a511-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9a511-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a511-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a511-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a511-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a511-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="9a511-120">Namespace</span></span><br/>                | <span data-ttu-id="9a511-121">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9a511-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9a511-122">MOF</span><span class="sxs-lookup"><span data-stu-id="9a511-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a511-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9a511-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a511-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9a511-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a511-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a511-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a511-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a511-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a511-127">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="9a511-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




