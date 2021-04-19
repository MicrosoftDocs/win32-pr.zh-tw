---
description: 重設虛擬鍵盤。
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
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987376"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="2484b-103">Msvm 鍵盤類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2484b-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="2484b-104">重設虛擬鍵盤。</span><span class="sxs-lookup"><span data-stu-id="2484b-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="2484b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2484b-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="2484b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2484b-106">Parameters</span></span>

<span data-ttu-id="2484b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2484b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2484b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2484b-108">Return value</span></span>

<span data-ttu-id="2484b-109">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="2484b-109">A return value of zero indicates success.</span></span> <span data-ttu-id="2484b-110">傳回值為1表示失敗，因為不支援此方法。</span><span class="sxs-lookup"><span data-stu-id="2484b-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="2484b-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2484b-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2484b-112">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2484b-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2484b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2484b-113">Requirements</span></span>



| <span data-ttu-id="2484b-114">需求</span><span class="sxs-lookup"><span data-stu-id="2484b-114">Requirement</span></span> | <span data-ttu-id="2484b-115">值</span><span class="sxs-lookup"><span data-stu-id="2484b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2484b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2484b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2484b-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2484b-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2484b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2484b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2484b-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2484b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2484b-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="2484b-120">Namespace</span></span><br/>                | <span data-ttu-id="2484b-121">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2484b-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2484b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="2484b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2484b-123"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2484b-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2484b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2484b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2484b-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2484b-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2484b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2484b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2484b-127">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="2484b-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




